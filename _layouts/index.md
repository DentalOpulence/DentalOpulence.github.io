---
layout: root
---
<div class="container-fluid bg-dark-not g-0">
<div class="container-fluid g-0">
<div id="carouselExampleSlidesOnly" class="carousel slide" data-bs-ride="carousel" data-bs-interval="5000" >
  <div class="carousel-inner">
      {% assign isfirst = true %}
      {% assign sorted_pages = site.pages | where:"type", "services" | sort: "sort" %}
      {% for p in sorted_pages %}
        <div class="carousel-item {% if isfirst == true %}active{% endif %}">
      <img src="{{p.hero-image}}" class="d-block w-100" alt="...">
      <div class="carousel-caption container notbg-frost rounded">
      <div class="mx-sm-5 px-sm-5">
        <h5>{{p.hero-heading}}</h5>
        <!--<p>{{p.hero-brief}}</p>-->
        <a class="btn btn-outline-light {{p.hero-button-class}}" href="{{p.url}}" role="button">{{p.hero-button}}</a>
      </div>
      </div>
    </div>
      {% assign isfirst = false %}
      {% endfor %}
    
  </div>
</div>
</div>

<div class="container-fluid notpt-3 bg-accent-prime-long-not g-0">

  <!--<div class="container py-1 py-sm-3">
      <div class="container text-light rounded p-0">
          <div class="p-3 px-5 px-sm-0">
              <div class="general-content">
                  {{content}}
              </div>
          </div>
      </div>
  </div>-->

  <div class="container g-0">
      {% assign sorted_pages = site.pages | where:"type", "services" | sort: "sort" %}
      {% for p in sorted_pages %}
      {% assign remainder = forloop.index | modulo: 2 %}
  <div class="container pt-3 pt-sm-5 text-light subsection g-5">
    <div class="row" style="background-color:{{p.subsection-color}}">
      {% if remainder == 1 %}
      <div class="col-md-6 bg-primary text-light g-0 d-block d-md-none">
        <img src="{{p.subsection-image}}" class="d-block w-100" alt="...">
      </div>
      <div class="col-md-6 p-0 my-0 px-md-5 my-md-5">
        <div class="p-5">
          <h2>{{p.subsection-heading}}</h2>
          <p>{{p.subsection-brief | markdownify}}</p>
          <a class="btn btn-outline-light {{p.subsection-button-class}}" href="{{p.url}}" role="button">{{p.subsection-button}}</a>
        </div>
      </div>
      <div class="col-md-6 bg-primary text-light g-0 d-none d-sm-none d-md-block">
        <img src="{{p.subsection-image}}" class="d-block w-100" alt="...">
      </div>
      {% else %}
      <div class="col-md-6 bg-primary text-light g-0">
        <img src="{{p.subsection-image}}" class="d-block w-100" alt="...">
      </div>
      <div class="col-md-6 p-0 my-0 px-md-5 my-md-5">
        <div class="p-5">
          <h2>{{p.subsection-heading}}</h2>
          <p>{{p.subsection-brief | markdownify}}</p>
          <a class="btn btn-outline-light {{p.subsection-button-class}}" href="{{p.url}}" role="button">{{p.subsection-button}}</a>
        </div>
      </div>
      
      {% endif %}
    </div>
  </div>
    
      {% if forloop.index == 2 %}

      {% include scrollingcards.html title="General Treatments" type="general-treatments" %}

      {% endif %}

            {% if forloop.index == 3 %}
      {% include scrollingcards.html title="Cosmetic Treatments" type="cosmetic-treatments" %}

      {% endif %}

      {% endfor %}



</div>

  </div>
</div>
