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
                <div class="col-lg-3 p-4 pb-0 bg-accent-secondary rounded d-none d-sm-block">
                    <div class="notpt-3">
                        {% include pagecards.html type=page.sidetype limit="3" %}
                    </div>
                </div>
            </div>
            <div class="row my-3">
            </div>
        </div>
    </div>
</div>