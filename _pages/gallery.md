---
title: "Gallery"
permalink: /gallery/
author_profile: true
---

# <font color="#004479">Gallery</font>
<span class='anchor' id='gallery'></span>

<div class="gallery-container">
  <div class="gallery-grid">
    {% for image in site.data.gallery %}
      <div class="gallery-item">
        <a href="{{ image.full_url }}" class="gallery-link" data-title="{{ image.title }}">
          <img src="{{ image.thumbnail_url }}" alt="{{ image.title }}" loading="lazy">
          <div class="gallery-item-info">
            <h3>{{ image.title }}</h3>
            <p>{{ image.description }}</p>
            <span class="gallery-date">{{ image.date }}</span>
          </div>
        </a>
      </div>
    {% endfor %}
  </div>
</div>

<style>
.gallery-container {
  padding: 20px 0;
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
  padding: 0 10px;
}

.gallery-item {
  position: relative;
  overflow: hidden;
  border-radius: 8px;
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
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: linear-gradient(transparent, rgba(0,0,0,0.8));
  color: white;
  padding: 15px;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.gallery-item:hover .gallery-item-info {
  opacity: 1;
}

.gallery-item-info h3 {
  margin: 0 0 5px 0;
  font-size: 1.2em;
}

.gallery-item-info p {
  margin: 0;
  font-size: 0.9em;
}

.gallery-date {
  font-size: 0.8em;
  opacity: 0.8;
}
</style> 