---
layout: root
---
<div class="container-fluid bg-dark g-0">
<div class="container-fluid g-0">
<div id="carouselExampleSlidesOnly" class="carousel slide" data-bs-ride="carousel" data-bs-interval="5000" >
  <div class="carousel-inner">
      {% assign isfirst = true %}
      {% assign sorted_pages = site.pages | where:"type", "nav-left" | sort: "sort" %}
      {% for p in sorted_pages %}
        <div class="carousel-item {% if isfirst == true %}active{% endif %}">
      <img src="{{p.hero-image}}" class="d-block w-100" alt="...">
      <div class="carousel-caption">
        <h5>{{p.hero-heading}}</h5>
        <p>{{p.hero-brief}}</p>
        <a class="btn btn-outline-light" href="{{p.url}}" role="button">{{p.hero-button}}</a>
      </div>
    </div>
      {% assign isfirst = false %}
      {% endfor %}
    
  </div>
</div>
</div>

<div class="container-fluid pt-3  bg-accent-prime-long g-0">
  <div class="container g-0">
    {{content}}


      {% assign sorted_pages = site.pages | where:"type", "nav-left" | sort: "sort" %}
      {% for p in sorted_pages %}
      {% assign remainder = forloop.index | modulo: 2 %}
  <div class="container py-5 text-light subsection g-5">
    <div class="row" style="background-color:{{p.subsection-color}}">
      {% if remainder == 1 %}
      <div class="col-md-6 bg-primary text-light g-0 d-block d-md-none">
        <img src="{{p.subsection-image}}" class="d-block w-100" alt="...">
      </div>
      <div class="col-md-6 p-0 my-0 p-md-5 my-md-5">
        <div class="p-5">
          <h2>{{p.subsection-heading}}</h2>
          <p>{{p.subsection-brief}}</p>
          <a class="btn btn-outline-light" href="{{p.url}}" role="button">{{p.subsection-button}}</a>
        </div>
      </div>
      <div class="col-md-6 bg-primary text-light g-0 d-none d-sm-none d-md-block">
        <img src="{{p.subsection-image}}" class="d-block w-100" alt="...">
      </div>
      {% else %}
      <div class="col-md-6 bg-primary text-light g-0">
        <img src="{{p.subsection-image}}" class="d-block w-100" alt="...">
      </div>
      <div class="col-md-6 p-0 my-0 p-md-5 my-md-5">
        <div class="p-5">
          <h2>{{p.subsection-heading}}</h2>
          <p>{{p.subsection-brief}}</p>
          <a class="btn btn-outline-light" href="{{p.url}}" role="button">{{p.subsection-button}}</a>
        </div>
      </div>
      
      {% endif %}
    </div>
  </div>
    
      {% if forloop.index == 1 %}
      <div class="container-fluid p-3 py-5 p-sm-5 text-light subsection-press">
  <div class="row">
    <h3 class="col-9 col-md-10 fs-3 fw-lighter">Press Releases</h3>
    <a class="mb-4 col-3 col-md-2 btn btn-outline-light" role="button">View All</a>
    <div class="row side-scroll">
    {% assign press_pages = site.pages | where:"type", "press" | sort: "sort" %}
    {% for p in press_pages limit:12 %}
    <div class="py-3 col-lg-3 col-md-6 col-sm-6">
      <p class="fs-6 fw-lighter">{{ p.date | date: '%B %d, %Y' }}</p>
      <p><a href="{{p.url}}" class="text-decoration-none text-light">{{p.brief}}</a></p>
    </div>
    {% endfor %}
    </div>
  </div>
</div>

      {% endif %}

            {% if forloop.index == 2 %}
      <div class="container-fluid p-3 py-5 p-sm-5 text-light subsection-blog">
  <div class="row">
    <h3 class="col-9 col-md-10 fs-3 fw-lighter">Blog Posts</h3>
    <a class="mb-4 col-3 col-md-2 btn btn-outline-light" role="button">View All</a>
    <div class="row side-scroll">
    {% assign blog_pages = site.pages | where:"type", "blog" | sort: "sort" %}
    {% for p in blog_pages limit:12 %}
    <div class="py-3 col-lg-3 col-md-6 col-sm-6">
      <p class="fs-6 fw-lighter">{{ p.date | date: '%B %d, %Y' }}</p>
      <p><a href="{{p.url}}" class="text-decoration-none text-light">{{p.title}}</a></p>
    </div>
    {% endfor %}
  </div>
  </div>
</div>

      {% endif %}

      {% endfor %}



</div>

  </div>
</div>