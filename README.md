# Zooming-Header


This code example is from the DevTips Live! episode. See a working example on [this blog post](http://travisneilson.com/workflow-tools/).


### The Markup (HMTL)
```
<header class="trike">
  <div></div>
</header>
```


### The Styles (SASS)
```
html, body
  height: 100%
  margin: 0
  padding: 0
  padding-bottom: 1000px

.trike
  position: relative
  height: 70%
  width: 100%
  
  > div
    +position(absolute, 0px 0px 0px 0px)
    background:
      image: url(../img/trike.jpg)
      size: cover
      position: center center
      repeat: no-repeat
```


### The Script (Javascript)
```
$(window).scroll(function() {

  var windowScroll = $(this).scrollTop();
  
  $('.trike > div').css({
    'top': '-' + windowScroll + 'px',
    'right': '-' + windowScroll + 'px',
    'left': '-' + windowScroll + 'px'
  });

});
```
