---
layout: root
---
<div class="container-fluid p-5 m-0" style="background: url({{page.hero-image}}) center; background-size: cover;">
    <div class="container-fluid p-5 py-md-5" style="background-image: linear-gradient(to right, rgba(0, 0, 0, 0), rgba(255, 0, 0, 0));">
        <div class="container p-5 py-md-5">
            <div class="row py-3 py-md-3">
                <div class="col-md-7">
                </div>
            </div>
        </div>
    </div>
</div>
<div class="container-fluid bg-dark py-3 py-md-5 bg-accent-prime">
    <div class="container bg-dark text-light rounded p-3 bg-content-prime">
        <nav aria-label="breadcrumb">
            <ol class="breadcrumb">
              <li class="breadcrumb-item"><a href="/index.html">Home</a></li>
              <li class="breadcrumb-item active" aria-current="page">{{page.title}}</li>
            </ol>
          </nav>
          <h1>{{page.title}}</h1>
          <p>{{page.hero-brief}}</p>
            {{content}}
            <div class="row my-3">
    </div></div>
</div>