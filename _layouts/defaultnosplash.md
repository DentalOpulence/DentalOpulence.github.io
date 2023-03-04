---
layout: root
---
<div class="container-fluid bg-dark py-3 py-md-5 bg-accent-prime pt-5">
    <div class="container-fluid pt-1 pt-sm-3">
        <div class="container bg-dark text-light rounded p-3 bg-content-prime mt-5">
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
            </div>
        </div>
    </div>
</div>