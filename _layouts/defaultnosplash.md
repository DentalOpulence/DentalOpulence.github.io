---
layout: root
---
<div class="container-fluid bg-dark py-3 py-md-5 bg-accent-prime pt-5 g-0">
    <div class="container pt-1 pt-sm-3">
        <div class="container bg-dark text-light rounded p-3 bg-content-prime mt-5">
            <div class="row p-sm-3">
                <div class="col-lg-9">
                    {% include breadcrumbs.html hidelast=page.breadcrumb-hidelast %}
                    <div class="general-content">
                        {{content}}
                    </div>
                </div>
                <div class="col-lg-3 notd-none notd-sm-block pt-5 pt-sm-0">
                    <p class="small">Also of interest ...</p>
                    <div class="notpt-3 p-4 pb-1 bg-accent-secondary rounded">
                        {% include pagecards.html type=page.sidetype limit="5" %}
                    </div>
                </div>
            </div>
            <div class="row my-3">
            </div>
        </div>
    </div>
</div>