---
layout: page
title: Projects
image: assets/images/lens08.JPG
nav-menu: true
---

<div class="container">
  <!-- Bio section -->
  <div class="bio-section">
    <p class="highlight-text">I work at the intersection of computer science, environmental science, and human well-being, developing AI systems that are sustainable, evidence-based, and human-centered. My interdisciplinary background allows me to bridge technical implementation with broader societal considerations, particularly in international and diverse team environments.</p>
  </div>

  <!-- Project filters -->
  <div class="filters">
    <ul class="actions">
      <li><a href="#" class="button small active" data-filter="all">All Projects</a></li>
      <li><a href="#" class="button small" data-filter="uni-assign">🎓 University Assignments</a></li>
      <li><a href="#" class="button small" data-filter="personal-project">🚀 Personal Projects</a></li>
      <li><a href="#" class="button small" data-filter="pro-proj">💼 Professional Projects</a></li>
      <li><a href="#" class="button small" data-filter="completed">Completed</a></li>
      <li><a href="#" class="button small" data-filter="in-progress">In Progress</a></li>
    </ul>
  </div>

  <!-- All Projects in one section -->
  <h2 class="section-title">My Projects</h2>
  <div class="row">
    {% assign all_projects = site.projects | sort: 'date' | reverse %}
    {% for project in all_projects %}
      {% if project.status %}
        {% assign project_status = project.status %}
      {% else %}
        {% if project.collection == 'ongoing_projects' %}
          {% assign project_status = 'In Progress' %}
        {% else %}
          {% assign project_status = 'Completed' %}
        {% endif %}
      {% endif %}

      {% assign status_class = project_status | downcase | replace: ' ', '-' %}
      {% assign project_type_class = project.project_type | downcase | replace: ' ', '-' %}
  
        {% if project.project_type == "University Assignment" %}
            {% assign project_type_display = "🎓 University Assignments" %}
            {% assign project_type_filter = "uni-assign" %}
        {% elsif project.project_type == "Personal Project" %}
            {% assign project_type_display = "🚀 Personal Projects" %}
            {% assign project_type_filter = "personal-project" %}
        {% elsif project.project_type == "Professional Project" %}
            {% assign project_type_display = "💼 Professional Projects" %}
            {% assign project_type_filter = "pro-proj" %}
        {% else %}
            {% assign project_type_display = project.project_type %}
            {% assign project_type_filter = project.project_type | downcase | replace: ' ', '-' %}
        {% endif %}
    
      <div class="col-md-4" 
        data-category="{{ project.category | downcase }}" 
        data-status="{{ project.status | downcase | replace: ' ', '-' }}"
        data-project-type="{{ project_type_filter }}">
        <article class="project-card {{ status_class }}">
          <a href="{{ site.baseurl }}{{ project.url }}">
            <h3>{{ project.title }}</h3>
            <hr>
            {% if project.image %}
            <img src="{{ site.baseurl }}/{{ project.image }}" alt="{{ project.title }}">
            {% endif %}
            
            <div class="tech-stack">
              <span class="tech">{{ project.tech_stack }}</span>
            </div>
            
            <p class="project-summary">{{ project.description | truncate: 120 }}</p>
            
            <div class="project-meta">
              <span class="category-tag">{{ project.category }}</span>
              <span class="status-tag {{ status_class }}">{{ project_status }}</span>
              {% if project.date %}
              <span class="date">{{ project.date | date: "%Y" }}</span>
              {% endif %}
            </div>
            
            <span class="read-more">Read more →</span>
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
  
  .bio-section {
    margin: 2em 0;
    padding: 1.5em;
    background-color: #f8f8f8;
    border-left: 4px solid #0085a1;
    border-radius: 4px;
  }
  
  .highlight-text {
    font-size: 1.2em;
    line-height: 1.5;
    margin: 0;
    color: #444;
  }
  
  .section-title {
    margin: 2em 0 1em;
    padding-bottom: 0.5em;
    border-bottom: 1px solid #eee;
    color: #333;
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
  
  .project-card {
    background-color: white;
    border-radius: 5px;
    overflow: hidden;
    box-shadow: 0 3px 10px rgba(0,0,0,0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    height: 100%;
    display: flex;
    flex-direction: column;
  }
  
  .project-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0,0,0,0.15);
  }
  
  .project-card.ongoing {
    border-top: 4px solid #0085a1;
  }
  
  .project-card a {
    display: flex;
    flex-direction: column;
    padding: 25px;
    text-decoration: none;
    color: inherit;
    height: 100%;
  }
  
  .project-card h3 {
    color: #333;
    font-size: 1.4rem;
    margin-top: 0;
    margin-bottom: 15px;
  }
  
  .project-card hr {
    width: 100%;
    border: none;
    height: 1px;
    background-color: #eee;
    margin: 0 0 20px;
  }
  
  .project-card img {
    width: 100%;
    height: 180px;
    object-fit: contain;
    border-radius: 4px;
    margin-bottom: 15px;
  }
  
  .tech-stack {
    margin-bottom: 15px;
  }
  
  .tech {
    font-style: italic;
    color: #666;
    font-size: 0.9rem;
  }
  
  .project-summary {
    flex-grow: 1;
    margin-bottom: 20px;
    color: #555;
    line-height: 1.5;
  }
  
  .project-meta {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 15px;
  }
  
  .category-tag {
    background-color: #f0f0f0;
    padding: 4px 8px;
    border-radius: 4px;
    font-size: 0.8rem;
    color: #555;
  }
  
  .status-tag {
    background-color: #0085a1;
    padding: 4px 8px;
    border-radius: 4px;
    font-size: 0.8rem;
    color: white;
  }
  
  .date {
    color: #999;
    font-size: 0.9rem;
  }
  
  .read-more {
    color: #0085a1;
    font-weight: 500;
    align-self: flex-end;
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
    margin: 0 5px 10px;
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
  
  /* Collaboration section */
  .collaboration-section {
    margin: 3em 0;
    padding: 2em;
    background-color: #f9f9f9;
    border-radius: 8px;
    text-align: center;
  }
  
  .collab-content {
    max-width: 800px;
    margin: 0 auto;
  }
  
  .collab-content p {
    margin-bottom: 1.5em;
  }
  
  .button.special {
    background-color: #0085a1;
    color: white;
    border-radius: 4px;
    text-decoration: none;
    font-weight: 500;
    display: inline-block;
    transition: background-color 0.3s ease;
  }
  
  .button.special:hover {
    background-color: #006d83;
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

    .project-type-tag {
    padding: 4px 8px;
    border-radius: 4px;
    font-size: 0.8rem;
    color: white;
    margin-right: 5px;
    }

    .project-type-tag.uni-assign {
    background-color: #9c27b0; /* Purple for university */
    }

    .project-type-tag.personal-project {
    background-color: #ff9800; /* Orange for personal */
    }

    .project-type-tag.pro-proj {
    background-color: #2196f3; /* Blue for professional */
    }
</style>

<!-- Filtering script -->
<script>
document.addEventListener('DOMContentLoaded', function() {
  const filterButtons = document.querySelectorAll('.filters a');
  const allProjectsButton = document.querySelector('.filters a[data-filter="all"]');
  
  // Keep track of active filters
  let activeFilters = {
    category: 'all',
    status: null,
    projectType: null
  };
  
  filterButtons.forEach(button => {
    button.addEventListener('click', function(e) {
      e.preventDefault();
      
      // Get the filter value
      const filter = this.getAttribute('data-filter');
      
      // First, remove active class from ALL buttons
      filterButtons.forEach(btn => {
        btn.classList.remove('active');
      });
      
      // Add active class to the clicked button
      this.classList.add('active');
      
      // Update active filters based on what was clicked
      if (filter === 'all') {
        // Reset all filters
        activeFilters = { 
          category: 'all', 
          status: null, 
          projectType: null 
        };
      } else if (filter === 'completed' || filter === 'in-progress') {
        // Update status filter
        activeFilters.status = filter;
        activeFilters.category = 'all'; // Keep showing all categories
        
        // If we have a project type filter active, highlight that button too
        if (activeFilters.projectType) {
          document.querySelector(`.filters a[data-filter="${activeFilters.projectType}"]`).classList.add('active');
        }
      } else if (filter === 'uni-assign' || filter === 'personal-project' || filter === 'pro-proj') {
        // Update project type filter
        activeFilters.projectType = filter;
        activeFilters.category = 'all'; // Keep showing all categories
        
        // If we have a status filter active, highlight that button too
        if (activeFilters.status) {
          document.querySelector(`.filters a[data-filter="${activeFilters.status}"]`).classList.add('active');
        }
      } else {
        // Update category filter
        activeFilters.category = filter;
        
        // Keep other filters active if they exist
        if (activeFilters.status) {
          document.querySelector(`.filters a[data-filter="${activeFilters.status}"]`).classList.add('active');
        }
        if (activeFilters.projectType) {
          document.querySelector(`.filters a[data-filter="${activeFilters.projectType}"]`).classList.add('active');
        }
      }
      
      // Only keep "All Projects" active if no other filters are selected
      if (filter !== 'all' && !activeFilters.status && !activeFilters.projectType && activeFilters.category === 'all') {
        allProjectsButton.classList.add('active');
      }
      
      // Apply the filters
      applyFilters();
    });
  });
  
  function applyFilters() {
    const projects = document.querySelectorAll('.col-md-4');
    
    projects.forEach(project => {
      const category = project.getAttribute('data-category');
      const status = project.getAttribute('data-status');
      const projectType = project.getAttribute('data-project-type');
      
      // Check if this project matches all active filters
      const matchesCategory = activeFilters.category === 'all' || category.includes(activeFilters.category);
      const matchesStatus = activeFilters.status === null || status === activeFilters.status;
      const matchesProjectType = activeFilters.projectType === null || projectType === activeFilters.projectType;
      
      if (matchesCategory && matchesStatus && matchesProjectType) {
        project.style.display = 'block';
      } else {
        project.style.display = 'none';
      }
    });
  }
});
</script>