---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<div class="posts-archive">
 

  <!-- 分类筛选 -->
  <div class="categories-filter">
    <div class="category-buttons">
      <button class="category-btn active" data-category="all">全部</button>
      {%- for category in site.categories -%}
        <button class="category-btn" data-category="{{ category[0] }}">{{ category[0] }} ({{ category[1] | size }})</button>
      {%- endfor -%}
    </div>
  </div>

  <!-- 文章列表 -->
  <div class="posts-list">
    {%- assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" -%}
    {%- for year_group in posts_by_year -%}
      <div class="year-section">
        <h2 class="year-heading">{{ year_group.name }}</h2>
        <div class="year-posts">
          {%- for post in year_group.items -%}
            <article class="post-item" data-categories="{{ post.categories | join: ' ' }}">
              <div class="post-date">
                <time datetime="{{ post.date | date_to_xmlschema }}">
                  {{ post.date | date: "%m月%d日" }}
                </time>
              </div>
              <div class="post-content">
                <h3 class="post-title">
                  <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
                </h3>
                {%- if post.excerpt -%}
                  <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
                {%- endif -%}
                <div class="post-meta-info">
                  {%- if post.categories.size > 0 -%}
                    <div class="post-categories">
                      {%- for category in post.categories -%}
                        <span class="category-tag">{{ category }}</span>
                      {%- endfor -%}
                    </div>
                  {%- endif -%}
                  {%- if post.tags.size > 0 -%}
                    <div class="post-tags">
                      {%- for tag in post.tags -%}
                        <span class="tag">{{ tag }}</span>
                      {%- endfor -%}
                    </div>
                  {%- endif -%}
                </div>
              </div>
            </article>
          {%- endfor -%}
        </div>
      </div>
    {%- endfor -%}
  </div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const categoryButtons = document.querySelectorAll('.category-btn');
  const postItems = document.querySelectorAll('.post-item');
  
  categoryButtons.forEach(button => {
    button.addEventListener('click', function() {
      const selectedCategory = this.getAttribute('data-category');
      
      // 更新按钮状态
      categoryButtons.forEach(btn => btn.classList.remove('active'));
      this.classList.add('active');
      
      // 筛选文章
      postItems.forEach(item => {
        const itemCategories = item.getAttribute('data-categories');
        if (selectedCategory === 'all' || itemCategories.includes(selectedCategory)) {
          item.style.display = 'flex';
        } else {
          item.style.display = 'none';
        }
      });
    });
  });
});
</script>

<style>
.posts-archive {
  max-width: 900px;
  margin: 0 auto;
}

.archive-stats {
  text-align: center;
  margin-bottom: 2rem;
  padding: 1rem;
  background: #f8f9fa;
  border-radius: 8px;
}

.categories-filter {
  margin-bottom: 3rem;
}

.categories-filter h3 {
  margin-bottom: 1rem;
  color: #2c3e50;
}

.category-buttons {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

.category-btn {
  padding: 8px 16px;
  border: 2px solid #667eea;
  background: transparent;
  color: #667eea;
  border-radius: 20px;
  cursor: pointer;
  transition: all 0.3s ease;
  font-weight: 500;
}

.category-btn:hover,
.category-btn.active {
  background: #667eea;
  color: white;
}

.year-section {
  margin-bottom: 1rem;
}

.year-heading {
  font-size: 1.5rem;
  color: #2c3e50;
  margin-bottom: 1rem;
  padding-bottom: 0.5rem;
  border-bottom: 3px solid #667eea;
  display: inline-block;
}

.post-item {
  display: flex;
  margin-bottom: 0.2rem;
  padding: 0.5rem;
  background: white;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  transition: all 0.3s ease;
  border-left: 12px solid transparent;
}

.post-item:hover {
  border-left-color: #667eea;
  box-shadow: 0 4px 8px rgba(0,0,0,0.15);
  transform: translateX(-25px);
}

.post-date {
  min-width: 80px;
  margin-right: 1.5rem;
}

.post-date time {
  color: #667eea;
  font-weight: 600;
}

.post-content {
  flex: 1;
}

.post-title {
  margin: 0 0 0.5rem 0;
}

.post-title a {
  color: #2c3e50;
  text-decoration: none;
  font-size: 1.2rem;
  font-weight: 600;
}

.post-title a:hover {
  color: #667eea;
}

.post-excerpt {
  color: #666;
  line-height: 1.5;
  margin-bottom: 1rem;
}

.post-meta-info {
  display: flex;
  gap: 15px;
  align-items: center;
  flex-wrap: wrap;
}

.post-categories,
.post-tags {
  display: flex;
  gap: 6px;
  flex-wrap: wrap;
}

@media (max-width: 768px) {
  .post-item {
    flex-direction: column;
  }
  
  .post-date {
    margin-right: 0;
    margin-bottom: 1rem;
  }
  
  .category-buttons {
    justify-content: center;
  }
}
</style> 