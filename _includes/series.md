
{% capture site_tags %}
{% for tag in site.tags %}
    {% if tag %}
        {{ tag | first }}
        {% unless forloop.last %}|{% endunless %}
    {% endif %}
{% endfor %}
{% endcapture %}
{% assign docs_tags = "" %}
{% for doc in site.docs %}
    {% assign ttags = doc.tags | join:'|' | append:'|' %}
    {% assign docs_tags = docs_tags | append:ttags %}
{% endfor %}
{% assign all_tags = site_tags | append:docs_tags %}
{% assign tags_list = all_tags | replace: "||", "|" | split:'|' | uniq | sort | compact %}
{% assign all_docs = site.docs | sort: "updated" | reverse %}
{% assign filtered_docs = all_docs %}

{% assign current_docs = "" | split: ',' %}
{% comment %}
    Any number of plan filters can be passed in via page.includeplans

    'any' acts like an 'or' and will match any tag
    'all' acts like an 'and' and doc must have all tags
{% endcomment %}

{% if page.includemethod == 'all' %}
    {% for doc in filtered_docs %}
    {% unless doc.tags contains "deprecated" %}
    {% assign uniquedoctags = doc.tags | uniq | sort %}

  

    {% assign concatplans = uniquedoctags | concat: page.includeplans | uniq %}
    {% comment %}
        To see if a document is a match, we'll concat page.includeplans and doc.tags --
        if they have the same number of tags, the document matches the filter so will be included
    {% endcomment %}
    {% if uniquedoctags.size == concatplans.size %}
    {% assign current_docs = current_docs | push: doc %}
    {% endif %}
    {% endunless %}
    {% endfor %}
{% else %}
    {% for doc in filtered_docs %}
    {% for includetag in page.includeplans %}
    {% unless doc.tags contains "deprecated" %}
    {% if doc.tags contains includetag %}
    {% assign current_docs = current_docs | push: doc %}
    {% endif %}
    {% endunless %}
    {% endfor %}
    {% endfor %}
{% endif %}

{% assign current_docs = current_docs | uniq %}

{% for doc in current_docs %}
{% assign uniquedoctags = doc.tags | uniq | sort %}

{% comment %}
    Filter tags for each doc, as specified in front matter
{% endcomment %}
{% assign filteredtags = "" | split: ',' %}
{% for tag in uniquedoctags %}
    {% assign foundFilteredTag = false %}
    {% for removetag in page.removetags %}
        {% if tag == removetag %}
           {% assign foundFilteredTag = true %}
        {% endif %}
    {% endfor %}
    {% if foundFilteredTag == false %}
        {% assign filteredtags = filteredtags | push: tag %}
    {% endif %}
{% endfor %}
{% assign filteredtags = filteredtags | uniq | sort %}

<div class="tag-entry" style="scroll-margin-top: 5rem;" id="{{ doc.title }}">
    <div>
        <a class="nav-entry" href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a> 
        {% if doc.updated %}
            <span class="docupdated"><time datetime="{{- doc.updated | date_to_xmlschema -}}"> {{- doc.updated | date: "%B %d, %Y" -}}</time></span>
        {% endif %}
    </div>
  
    <div style="padding-bottom: 5px;">{% for tag in filteredtags %}<span style="font-size:12px" class="badge badge-{{ site.tag_color }}"><a style="cursor:pointer; color:white" href="{% if site.tag_search_endpoint %}{{ site.tag_search_endpoint }}{{ tag }}{% else %}{{ site.url }}{{ site.baseurl }}/tags#{{ tag }} {% endif %}">{{ tag }}</a></span>{% endfor %}</div>
    <div>
    {% if doc.youtubeid %}<a href="https://www.youtube.com/watch?v={{ doc.youtubeid }}"><img width="160" src="https://img.youtube.com/vi/{{ doc.youtubeid }}/0.jpg" style="float:left; padding-right:15px;"/></a>
    {% endif %}
    {{ doc.description }} 
    <a href="{{- site.baseurl -}}{{- doc.url -}}">more &#187;</a> 
    </div>
</div>

<div style="clear:both; padding-top: 20px; padding-bottom: 0px;">
<hr/>
</div>

{% endfor %}