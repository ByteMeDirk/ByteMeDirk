---
layout: default
title: Projects
permalink: /projects/
---

<h1 class="display-4 text-gradient mb-5">Projects & Portfolio</h1>

<p class="lead mb-5">Explore a selection of my data engineering and development projects.</p>

<!-- Featured Projects -->
<div class="row mb-5">
  {% assign featured_projects = site.data.projects | where: "featured", true %}
  {% for project in featured_projects %}
    <div class="col-md-6 col-lg-4 mb-4">
      <div class="card bg-dark-glass h-100 border-glow cert-card">
        {% if project.image %}
          <div class="card-img-top-container">
            <div class="card-img-overlay-effect"></div>
            <img src="{{ project.image | relative_url }}" class="card-img-top" alt="{{ project.name }}">
          </div>
        {% endif %}
        <div class="card-body">
          <h3 class="h5 card-title">{{ project.name }}</h3>
          <p class="card-text small text-light-muted">{{ project.description }}</p>
          <div class="mb-3">
            {% for tech in project.technologies %}
              <span class="badge bg-tech me-1 mb-1">{{ tech }}</span>
            {% endfor %}
          </div>
          {% if project.url %}
            <a href="{{ project.url }}" class="btn btn-outline-primary btn-sm" target="_blank">
              <i class="fas fa-code-branch me-2"></i>View Project
            </a>
          {% endif %}
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<!-- All Projects -->
<div class="card bg-dark-glass mb-5 border-glow">
  <div class="card-body">
    <h2 class="card-title section-title mb-4">
      <i class="fas fa-laptop-code me-2 text-primary"></i>All Projects
    </h2>
    
    <div class="table-responsive">
      <table class="table table-dark table-hover">
        <thead>
          <tr>
            <th scope="col">Project</th>
            <th scope="col">Description</th>
            <th scope="col">Technologies</th>
            <th scope="col">Link</th>
          </tr>
        </thead>
        <tbody>
          {% for project in site.data.projects %}
            <tr>
              <td>{{ project.name }}</td>
              <td class="text-light-muted small">{{ project.description | truncate: 100 }}</td>
              <td>
                {% for tech in project.technologies limit:3 %}
                  <span class="badge bg-tech-secondary me-1">{{ tech }}</span>
                {% endfor %}
                {% if project.technologies.size > 3 %}
                  <span class="badge bg-secondary">+{{ project.technologies.size | minus: 3 }}</span>
                {% endif %}
              </td>
              <td>
                {% if project.url %}
                  <a href="{{ project.url }}" class="btn btn-outline-primary btn-sm" target="_blank">
                    <i class="fas fa-external-link-alt"></i>
                  </a>
                {% endif %}
              </td>
            </tr>
          {% endfor %}
        </tbody>
      </table>
    </div>
  </div>
</div>

<!-- GitHub Activity -->
<div class="card bg-dark-glass mb-5 border-glow">
  <div class="card-body">
    <h2 class="card-title section-title mb-4">
      <i class="fab fa-github me-2 text-primary"></i>GitHub Activity
    </h2>
    <div class="text-center">
      <div class="row">
        <div class="col-md-6 mb-4">
          <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=ByteMeDirk&layout=compact&theme=dark&bg_color=00000000" alt="Top Languages" class="img-fluid github-stats">
        </div>
        <div class="col-md-6 mb-4">
          <img src="https://github-readme-stats.vercel.app/api?username=ByteMeDirk&show_icons=true&count_private=true&theme=dark&bg_color=00000000" alt="GitHub Stats" class="img-fluid github-stats">
        </div>
      </div>
      <p class="text-light-muted mt-3"><em>Note: Most of my professional work is not on GitHub, so this may not fully represent my coding activity.</em></p>
    </div>
  </div>
</div>
