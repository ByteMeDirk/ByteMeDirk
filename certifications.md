---
layout: default
title: Certifications
permalink: /certifications/
---

<h1 class="display-4 text-gradient mb-5">Certifications & Education</h1>

<p class="lead mb-5">A comprehensive collection of my professional certifications, academic achievements, and continuous learning journey.</p>

<!-- University Education -->
<div class="card bg-dark-glass mb-5 border-glow">
  <div class="card-body">
    <h2 class="card-title section-title mb-4">
      <i class="fas fa-university me-2 text-primary"></i>University Education
    </h2>
    
    <div class="row g-4">
      {% for cert in site.data.certifications %}
        {% if cert.type == "university" %}
          <div class="col-md-6">
            <div class="card bg-dark cert-card border-light-subtle h-100">
              <div class="card-body">
                <div class="d-flex align-items-center mb-3">
                  {% if cert.issuerLogo %}
                    <img src="{{ cert.issuerLogo | relative_url }}" alt="{{ cert.issuer }}" class="cert-issuer-icon me-3">
                  {% else %}
                    <div class="cert-issuer-icon me-3 d-flex align-items-center justify-content-center bg-primary bg-opacity-10 rounded-circle">
                      <i class="fas fa-university text-primary"></i>
                    </div>
                  {% endif %}
                  <h3 class="h5 mb-0">{{ cert.name }}</h3>
                </div>
                <p class="text-light-muted mb-2">{{ cert.issuer }}</p>
                <p class="text-light-muted small mb-3">{{ cert.date }}</p>
                {% if cert.description %}
                  <p class="small mb-3">{{ cert.description }}</p>
                {% endif %}
                {% if cert.url %}
                  <a href="{{ cert.url }}" class="btn btn-outline-primary btn-sm" target="_blank">
                    <i class="fas fa-external-link-alt me-2"></i>View Credential
                  </a>
                {% endif %}
              </div>
            </div>
          </div>
        {% endif %}
      {% endfor %}
    </div>
  </div>
</div>

<!-- LinkedIn Learning -->
<div class="card bg-dark-glass mb-5 border-glow">
  <div class="card-body">
    <h2 class="card-title section-title mb-4">
      <i class="fab fa-linkedin me-2 text-primary"></i>LinkedIn Learning
    </h2>
    
    <div class="row g-4">
      {% for cert in site.data.certifications %}
        {% if cert.type == "linkedin" %}
          <div class="col-md-6 col-lg-4">
            <div class="card bg-dark cert-card border-light-subtle h-100">
              <div class="card-body">
                <div class="d-flex align-items-center mb-3">
                  <div class="cert-issuer-icon me-3 d-flex align-items-center justify-content-center bg-primary bg-opacity-10 rounded-circle">
                    <i class="fab fa-linkedin text-primary"></i>
                  </div>
                  <h3 class="h6 mb-0">{{ cert.name }}</h3>
                </div>
                <p class="text-light-muted small mb-3">{{ cert.date }}</p>
                {% if cert.url %}
                  <a href="{{ cert.url }}" class="btn btn-outline-primary btn-sm" target="_blank">
                    <i class="fas fa-external-link-alt me-2"></i>View Credential
                  </a>
                {% endif %}
              </div>
            </div>
          </div>
        {% endif %}
      {% endfor %}
    </div>
  </div>
</div>

<!-- Coursera -->
<div class="card bg-dark-glass mb-5 border-glow">
  <div class="card-body">
    <h2 class="card-title section-title mb-4">
      <i class="fas fa-graduation-cap me-2 text-primary"></i>Coursera
    </h2>
    
    <div class="row g-4">
      {% for cert in site.data.certifications %}
        {% if cert.type == "coursera" %}
          <div class="col-md-6 col-lg-4">
            <div class="card bg-dark cert-card border-light-subtle h-100">
              <div class="card-body">
                <div class="d-flex align-items-center mb-3">
                  <div class="cert-issuer-icon me-3 d-flex align-items-center justify-content-center bg-primary bg-opacity-10 rounded-circle">
                    <i class="fas fa-certificate text-primary"></i>
                  </div>
                  <h3 class="h6 mb-0">{{ cert.name }}</h3>
                </div>
                <p class="text-light-muted small mb-2">{{ cert.issuer }}</p>
                <p class="text-light-muted small mb-3">{{ cert.date }}</p>
                {% if cert.url %}
                  <a href="{{ cert.url }}" class="btn btn-outline-primary btn-sm" target="_blank">
                    <i class="fas fa-external-link-alt me-2"></i>View Credential
                  </a>
                {% endif %}
              </div>
            </div>
          </div>
        {% endif %}
      {% endfor %}
    </div>
  </div>
</div>

<!-- Industry Certifications -->
<div class="card bg-dark-glass mb-5 border-glow">
  <div class="card-body">
    <h2 class="card-title section-title mb-4">
      <i class="fas fa-award me-2 text-primary"></i>Industry Certifications
    </h2>
    
    <div class="row g-4">
      {% for cert in site.data.certifications %}
        {% if cert.type == "industry" %}
          <div class="col-md-6">
            <div class="card bg-dark cert-card border-light-subtle h-100">
              <div class="card-body">
                <div class="d-flex align-items-center mb-3">
                  {% if cert.issuerLogo %}
                    <img src="{{ cert.issuerLogo | relative_url }}" alt="{{ cert.issuer }}" class="cert-issuer-icon me-3">
                  {% else %}
                    <div class="cert-issuer-icon me-3 d-flex align-items-center justify-content-center bg-primary bg-opacity-10 rounded-circle">
                      <i class="fas fa-award text-primary"></i>
                    </div>
                  {% endif %}
                  <h3 class="h5 mb-0">{{ cert.name }}</h3>
                </div>
                <p class="text-light-muted mb-2">{{ cert.issuer }}</p>
                <p class="text-light-muted small mb-3">{{ cert.date }}</p>
                {% if cert.description %}
                  <p class="small mb-3">{{ cert.description }}</p>
                {% endif %}
                {% if cert.url %}
                  <a href="{{ cert.url }}" class="btn btn-outline-primary btn-sm" target="_blank">
                    <i class="fas fa-external-link-alt me-2"></i>View Credential
                  </a>
                {% endif %}
              </div>
            </div>
          </div>
        {% endif %}
      {% endfor %}
    </div>
  </div>
</div>

<!-- Other Online Courses -->
<div class="card bg-dark-glass mb-5 border-glow">
  <div class="card-body">
    <h2 class="card-title section-title mb-4">
      <i class="fas fa-laptop-code me-2 text-primary"></i>Other Online Courses
    </h2>
    
    <div class="row g-4">
      {% for cert in site.data.certifications %}
        {% if cert.type == "other" %}
          <div class="col-md-6 col-lg-4">
            <div class="card bg-dark cert-card border-light-subtle h-100">
              <div class="card-body">
                <div class="d-flex align-items-center mb-3">
                  <div class="cert-issuer-icon me-3 d-flex align-items-center justify-content-center bg-primary bg-opacity-10 rounded-circle">
                    <i class="fas fa-laptop-code text-primary"></i>
                  </div>
                  <h3 class="h6 mb-0">{{ cert.name }}</h3>
                </div>
                <p class="text-light-muted small mb-2">{{ cert.issuer }}</p>
                <p class="text-light-muted small mb-3">{{ cert.date }}</p>
                {% if cert.url %}
                  <a href="{{ cert.url }}" class="btn btn-outline-primary btn-sm" target="_blank">
                    <i class="fas fa-external-link-alt me-2"></i>View Credential
                  </a>
                {% endif %}
              </div>
            </div>
          </div>
        {% endif %}
      {% endfor %}
    </div>
  </div>
</div>
