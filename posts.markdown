---
layout: page
permalink: /posts/
---

{%- if site.posts.size > 0 -%}
  
  {%- assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" -%}
  {%- for year_group in posts_by_year -%}
    
## {{ year_group.name }}

{%- for post in year_group.items -%}
**{{ post.date | date: "%m月%d日" }}** - [{{ post.title | escape }}]({{ post.url | relative_url }})
{%- if post.categories.size > 0 -%} · {{ post.categories | join: ", " }}{%- endif -%}
{%- if post.excerpt -%}  
{{ post.excerpt | strip_html | truncatewords: 25 }}
{%- endif -%}

{%- endfor -%}
  {%- endfor -%}
  
{%- else -%}
  暂无文章。
{%- endif -%} 