---
title: "Gallery"
permalink: /gallery/
author_profile: false
layout: default
---

<style>
/* 导航栏样式 */
.masthead {
  border-bottom: 1px solid #f2f3f3;
  background: white;
}

.masthead__menu {
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 1em;
}

.greedy-nav {
  display: flex;
  align-items: center;
}

.visible-links {
  display: flex;
  justify-content: flex-start;
  flex-wrap: nowrap;
  margin: 0;
  padding: 0;
  list-style: none;
  width: 100%;
}

.masthead__menu-item {
  padding: 0.5em 1em;
  white-space: nowrap;
}

.masthead__menu-item:first-child {
  padding-left: 0;
}

/* 导航链接样式 */
.masthead__menu-item a {
  color: #494e52;
  text-decoration: none;
  font-family: -apple-system, BlinkMacSystemFont, "Roboto", "Segoe UI", "Helvetica Neue", "Lucida Grande", Arial, sans-serif;
  font-size: 16px;
  font-weight: normal;
}

.masthead__menu-item a:hover {
  color: #000;
  text-decoration: none;
}

/* 移除原有的左侧空间 */
.page {
  width: 100%;
  padding-right: 0;
  margin: 0;
}

#main {
  max-width: 1280px;
  margin: 0 auto;
  padding: 1em;
}

/* 调整导航栏容器宽度 */
.initial-content {
  max-width: 1280px;
  margin: 0 auto;
}
</style>

<div class="gallery-container">
  <div class="gallery-grid">
    {% for image in site.data.gallery %}
      <div class="gallery-item">
        <img src="{{ image.image }}" alt="{{ image.title }}" loading="lazy">
        <div class="gallery-item-info">
          <h3>{{ image.title }}</h3>
          <p>{{ image.description }}</p>
        </div>
      </div>
    {% endfor %}
  </div>
</div>

<style>
.gallery-container {
  padding: 20px 0;
  max-width: 1280px;
  margin: 0 auto;
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 30px;
  padding: 0 10px;
}

.gallery-item {
  position: relative;
  overflow: hidden;
  border-radius: 8px;
  background: white;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.gallery-item:hover {
  transform: translateY(-5px);
}

.gallery-item img {
  width: 100%;
  height: 250px;
  object-fit: cover;
  display: block;
}

.gallery-item-info {
  padding: 15px;
  background: white;
}

.gallery-item-info h3 {
  margin: 0 0 10px 0;
  font-size: 1.2em;
  color: #333;
  font-weight: 500;
}

.gallery-item-info p {
  margin: 0;
  font-size: 0.95em;
  color: #666;
  line-height: 1.5;
}
</style> 