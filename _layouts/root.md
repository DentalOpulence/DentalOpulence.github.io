---
---
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>{{page.title}}</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-gH2yIJqKdNHPEq0n4Mqa/HGKIhSkIHeL5AyhkYV8i59U5AR6csBvApHHNl/vI1Bx" crossorigin="anonymous">
    <link href="/css/styles.css" rel="stylesheet">
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&display=swap" rel="stylesheet">
  </head>
  <body>
  <nav class="p-3 navbar header fixed-top navbar-expand-lg bg-light">
  <div class="container-fluid">
    <a class="navbar-brand py-1 logo pe-4" href="/"><span class="svglogo"><svg xmlns="http://www.w3.org/2000/svg" width="60" viewBox="0 0 392 203"><path d="M189,101.5A101.5,101.5,0,1,1,290.5,203,101.5,101.5,0,0,1,189,101.5ZM0,203V0H75.443A102.392,102.392,0,0,1,95.91,2.062a101.052,101.052,0,0,1,36.314,15.273,101.8,101.8,0,0,1,36.795,44.656,101,101,0,0,1,5.917,19.053,102.455,102.455,0,0,1,0,40.911,100.913,100.913,0,0,1-15.281,36.293,101.843,101.843,0,0,1-44.682,36.774,101.09,101.09,0,0,1-19.063,5.915A102.392,102.392,0,0,1,75.443,203Z"/></svg><span class="tm">&reg;</span></span>Dental Opulence<!--&reg;--><!--<span class="fs-6 fw-light">&reg;</span>--></a>
    <button class="navbar-toggler bg-light" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse py-5 py-md-3" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
      {% include navleft.html %}
      </ul>
      <ul class="navbar-nav d-lg-none d-xl-flex">
      {% include navright.html %}
        </ul>    </div>
  </div>
</nav>
    {{content}}

{% include footer.html %}


    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/js/bootstrap.bundle.min.js" integrity="sha384-A3rJD856KowSb7dwlZdYEkO39Gagi7vIsF0jrRAoQmDKKtQBHUuLZ9AsSv4jD4Xa" crossorigin="anonymous"></script>
    
        <script>
var scrollDir = (function (oldOffset, lastOffset, oldDir) {
    return function (offset) {

        var dir = offset < oldOffset;
        if (dir !== oldDir) {
            lastOffset = offset;
        } else {
            offset = offset - height;
        }
        oldOffset = offset;
        oldDir = dir;
        return {
            dir: dir,
            last: lastOffset
        };
    };
}());

var header = document.querySelector('.headerss');
var height = header.clientHeight;

$(window).scroll(function () {
    var scrollY = $(window).scrollTop();
    var dir = scrollDir(scrollY);
    var diff = dir.last - scrollY;

    var max = Math.max(-height, Math.min(height, diff));
    
    max = (dir.dir ? max - height : max); 
    max = scrollY<height?0:max;
    

    $('.headerss').data('size', 'small');
    $('.headerss').stop().animate({
        top: max
    }, 60);


});
        </script>
  </body>
</html>