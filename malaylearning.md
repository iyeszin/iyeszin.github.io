---
layout: page
title: Malay learning for adults
description: A structured approach to learning Malay for adult learners
---

<div class="container">
  <!-- Language level filters -->
  <div class="filters">
    <ul class="actions">
      <li><a href="#" class="button small active" data-filter="all">All Lessons</a></li>
      <li><a href="#" class="button small" data-filter="a1">A1 Beginner</a></li>
      <li><a href="#" class="button small" data-filter="a2">A2 Elementary</a></li>
      <li><a href="#" class="button small" data-filter="b1">B1 Intermediate</a></li>
      <li><a href="#" class="button small" data-filter="culture">Culture</a></li>
    </ul>
  </div>

  <div class="row">
    {% assign sorted_posts = site.malay_learning | sort: 'lesson_number' %}
    {% for post in sorted_posts %}
    {% assign levels = post.level | downcase | replace: ' ', '' | split: ',' %}
    {% assign category = post.categories | first | downcase %}
    <div class="col-md-4" 
         data-levels="{{ levels | join: ',' }}" 
         data-category="{{ category }}">
      <article class="malay-post">
        <a href="{{ site.baseurl }}{{ post.url }}">
          <h2>{{ post.title }}</h2>
          <hr>
          {% if post.image %}
          <img src="{{ site.baseurl }}/{{ post.image }}" alt="{{ post.title }}">
          {% endif %}
          
          <div class="post-meta">
            <div class="level-lesson">
              <span class="level">{{ post.level }}</span>
              {% if post.lesson_number %}
              <span class="lesson">Lesson {{ post.lesson_number }}</span>
              {% endif %}
            </div>
            <div class="date">{{ post.date | date: "%B %d, %Y" }}</div>
          </div>
        </a>
      </article>
    </div>
    {% endfor %}
  </div>
</div>

<style>
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 15px;
  }
  
  .row {
    display: flex;
    flex-wrap: wrap;
    margin: 0 -15px;
  }
  
  .col-md-4 {
    flex: 0 0 calc(33.333% - 30px);
    max-width: calc(33.333% - 30px);
    margin: 0 15px 30px;
  }
  
  .malay-post {
    background-color: white;
    border-radius: 5px;
    overflow: hidden;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    transition: transform 0.3s ease;
    height: 100%;
  }
  
  .malay-post:hover {
    transform: translateY(-5px);
  }
  
  .malay-post a {
    display: block;
    padding: 25px;
    text-decoration: none;
    color: inherit;
    height: 100%;
  }
  
  .malay-post h2 {
    text-align: center;
    color: #666;
    font-size: 1.5rem;
    margin-top: 0;
  }
  
  .malay-post hr {
    width: 100%;
    border: none;
    height: 1px;
    background-color: #ddd;
    margin: 15px 0 20px;
  }
  
  .malay-post img {
    width: 100%;
    height: auto;
    display: block;
    margin: 0 auto;
  }
  
  .post-meta {
    margin-top: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .level-lesson {
    display: flex;
    gap: 10px;
  }
  
  .level {
    font-weight: bold;
    color: #0085a1;
  }
  
  .lesson {
    color: #666;
  }
  
  .date {
    color: #999;
    font-size: 0.9rem;
  }
  
  /* Filter styles */
  .filters {
    margin: 2em 0;
  }
  
  .filters .actions {
    justify-content: center;
    display: flex;
    list-style: none;
    padding: 0;
    flex-wrap: wrap;
  }
  
  .filters .button {
    margin: 0 5px;
    /* padding: 8px 8px; */
    background-color: #f5f5f5;
    color: #666;
    border-radius: 4px;
    font-size: 0.9rem;
    cursor: pointer;
    transition: all 0.3s ease;
    text-decoration: none;
    display: inline-block;
  }
  
  .filters .button:hover {
    background-color: #e0e0e0;
  }
  
  .filters .button.active {
    background-color: #0085a1;
    color: white;
  }
  
  @media (max-width: 992px) {
    .col-md-4 {
      flex: 0 0 calc(50% - 30px);
      max-width: calc(50% - 30px);
    }
  }
  
  @media (max-width: 576px) {
    .col-md-4 {
      flex: 0 0 calc(100% - 30px);
      max-width: calc(100% - 30px);
    }
    
    .filters .actions {
      justify-content: flex-start;
    }
  }
</style>

<!-- Simple filtering script -->
<script>
document.addEventListener('DOMContentLoaded', function() {
  const filterButtons = document.querySelectorAll('.filters a');
  
  filterButtons.forEach(button => {
    button.addEventListener('click', function(e) {
      e.preventDefault();
      
      // Remove active class from all buttons
      filterButtons.forEach(btn => btn.classList.remove('active'));
      
      // Add active class to clicked button
      this.classList.add('active');
      
      const filter = this.getAttribute('data-filter');
      const posts = document.querySelectorAll('.col-md-4');
      
      posts.forEach(post => {
        const levels = post.getAttribute('data-levels');
        const category = post.getAttribute('data-category');
        
        // Show post if:
        // 1. Filter is "all", OR
        // 2. Post has the selected level, OR
        // 3. Filter matches the post's category
        if (filter === 'all' || 
            (levels && levels.split(',').includes(filter)) ||
            (filter === category)) {
          post.style.display = 'block';
        } else {
          post.style.display = 'none';
        }
      });
    });
  });
});
</script>