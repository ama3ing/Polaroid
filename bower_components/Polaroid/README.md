Polaroid
========

jQuery plugin to create some old school polaroid images


Installation
------------

Download the plugin [zipball](https://github.com/me1ifaro/Polaroid/archive/master.zip) or you can install it using bower

```sh

$ bower install Polaroid
```

I suggest using [velocity](https://github.com/julianshapiro/velocity) instead of standard ```jQuery.animate()```
All you have to do is include ```velocity.js``` somewhere in your page.


Usage
-----

Usage of this plugin is very easy, I promise.

### Step 1

Include it in your page

```html
<script type="text/javascript" src="path/to/polaroid.js">
```

### Step 2

Create easy markup

```html
<div class="my-awesome-images">
    <img src="path/to/image.jpg" alt="My awesome image #1" />
    ...
</div>
```

### Step 3

Time to rock

```javascript

$('.my-awesome-images').polaroid();
```

### Step 4

Enjoy

Captions
--------

Captions can be set by using ```data-caption``` attribute for example:
```html
<img src="path/to/image.jpg" alt="My awesome image #1" data-caption="<h3>Me and Mary on vacation</h3>" />
```

Config reference
----------------

Below there is default configuration of Polaroid feel free to override

```json
{
    autoPlay: false,
    duration: 2000,
    slideBackground: "base64 encoded background or url to background",
    rotationRange: {
        min: -7,
        max: 7
    },
    shadow: '5px 5px 3px rgba(0,0,0,0.15)',
    borderRadius: '2px'
}
```

```javascript

$('.my-awesome-images').polaroid({
    autoPlay:true,
    duration:5000
});
```

Advanced usage
--------------

If you want to use Polaroid with require js modify file as following

 ```javascript
define(['vendor/velocity/jquery.velocity', 'jquery'], function() {
    "use strict";
        $.fn.polaroid = function(config) {
        ...
}
 ```