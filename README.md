# Scrolly.js
You can create a rich and **storytelling animated web pages** with up and down scrolling 👋
Visitors can feel the page with scrolling and it has a really minimal learning curve.

Scrolly.js plugin is proudly created and maintained by [cssanimation.io](http://cssanimation.io/) team, that a web based open source animation library by a team of **passionate web animation lover**.

We developed the most easier way to work with scroll animation, Just use `data-scrolly-top` and `data-scrolly-down` attribute to quickly build powerful templates of your own.

# How To Use It?
**Include Library:** To get started, just download `scrolly.js` and `cssanimation.css` [download](http://cssanimation.io/). Now include the `cssanimation.css` stylesheet into the head and add `scrolly.js` scripts before the `body` tag
``` html
<!DOCTYPE html>
<html lang="en">
<head> 
    <meta charset="UTF-8">
    <title>Document</title>
    <link rel="stylesheet" href="scrolly/cssanimation.css"> 
</head>
<body> 
 

    <script type="text/javascript" src="scrolly/scrolly.js"></script>
</body>
</html>
```

**Activate Now:** when done with including stuff, time to activate scrolly.js
``` html
<!DOCTYPE html>
<html lang="en">
<head> 
    <meta charset="UTF-8">
    <title>Document</title>
    <link rel="stylesheet" href="scrolly/cssanimation.css"> 
</head>
<body> 
 

    <script type="text/javascript" src="scrolly/scrolly.js"></script>
    <script>
       window.onload = function() {
          scrolly();
       }; 
    </script>
</body>
</html>
```


**Define DOWN Animation:** Once you've done that, define animation class name in `data-scrolly-down` attribute like the example below to the element **that you want to animate when the page scroll to DOWN**. here we are using `blurInTop`.

``` html
<div data-scrolly-down="blurInTop"> 
     it's easy to do 
</div>
```

**Define TOP Animation:** Like the DOWN animation, to animate element **while scrollig to TOP**, just use `data-scrolly-top` attribute and add whatever animation you want. We used `blurInBottom` for example.

``` html
<div data-scrolly-top="blurInBottom"> 
     it's easy to do 
</div>
```

**Use Both DOWN and TOP Animation:** You can also trigger an animation effect in any given element from both **DOWN & TOP**, means it will animate on both scrolling **DOWN & TOP**. See the example below-

``` html
<div data-scrolly-top="blurInBottom" data-scrolly-down="blurInTop"> 
     it's easy to do 
</div>
```

**Use Animation on Character:** Yes!! you can now animate each character of any sentences while you scroll. Add `data-scrolly-characters="sequential"` for sequential animation of the characters or `data-scrolly-characters="random"` if you want it to animate it in random order.... **isn't it exciting !!**
``` html
<h1 data-scrolly-characters="sequentially" data-scrolly-down="leSpinInRight" data-scrolly-top="leSpinInLeft">
     I am Awesome. I can animate every characters in a sentence
</h1>

<h1 data-scrolly-characters="randomly" data-scrolly-down="leSpinInRight" data-scrolly-top="leSpinInLeft">
     I am Awesome. I can animate every characters in a sentence
</h1>
```

**Add Delay in Character Animation:** You can add dealy on character animation by adding `data-scrolly-characters="delay:100"` attribute.
``` html
<h1 data-scrolly-characters="sequentially" data-scrolly-characters="delay:100" data-scrolly-down="leSpinInRight" data-scrolly-top="leSpinInLeft">
     I am Awesome. I can animate every characters in a sentence
</h1>

<h1 data-scrolly-characters="randomly" data-scrolly-characters="delay:100" data-scrolly-down="leSpinInRight" data-scrolly-top="leSpinInLeft">
     I am Awesome. I can animate every characters in a sentence
</h1>
```

**Use Animation Duration:** Default animation duration is `1s` but you can always define your custom duration by adding `duration:[number]s` attribute.
``` html
<div data-scrolly-down="blurInTop, duration:2s"> 
     it's easy to do 
</div>
```

**Add Delay:** By adding the attribute `delay:[number]s` you can set a delay time to start of an animation.
``` html
<div data-scrolly-down="blurInTop, delay:2s"> 
     I am start after 2s 
</div>
```

**Infinite or Specify The Number of Animation:** The `iteration-count` specifies the number of times an animation should be played. Use `iteration-count: 3` if you want to animate 3 times or use `iteration-count:infinite` which should play the animation with no limit.
``` html
<div data-scrolly-down="blurInTop, iteration-count:3"> 
     I am animate 3 times 
</div>

<div data-scrolly-down="blurInTop, iteration-count:infinite"> 
     I am animate unlimited times 
</div>
```

**Animation Direction:** You can run the animation in reverse direction or alternate cycle **(forward, backward, then again forward)** using `direction` attribute.
``` html
<div data-scrolly-down="blurInTop, direction:reverse"> 
     it's easy to do 
</div>

<div data-scrolly-top="moveFromRight, iteration-count:3, direction:alternate"> 
     it's easy to do 
</div>
```

**Timing Function:** You can add all CSS pre-defined speed curve `ease, ease-in, ease-out, linear` of an animation or define your own values with a `cubic-bezier` function by adding `timing-function` attribute.
``` html
<div data-scrolly-down="blurInTop, timing-function:linear"> 
     it's easy to do 
</div>

<div data-scrolly-down="blurInTop, timing-function:cubic-bezier(.17,.67,.83,.67)"> 
     it's easy to do 
</div>
```

**Define Top Offset Value:** Set the top animation starting point after it appears on the browser window `data-scrolly-offset-top="300px"`.
``` html
<div data-scrolly-down="blurInTop" data-scrolly-offset-top="300px">
     it's easy to do 
</div>
```

**Define Bottom Offset Value:** Like the top offset the `data-scrolly-offset-bottom="500px"` attribute can be used to set the bottom starting point of the animation.
``` html
<div data-scrolly-down="blurInBottom" data-scrolly-offset-bottom="500px">
     it's easy to do 
</div>
```

**On Click Animtion:** Initiate the animation with on click event using by `data-scrolly-click="fadeIn"`.
``` html
<div data-scrolly-down="blurInBottom" data-scrolly-click="fadeIn"> 
     I am animate when you click me. Please click 
</div>
```

**Mouse Over Animtion:** For mouse over animation add the `data-scrolly-mouseover="zoomIn"` attribute
``` html
<div data-scrolly-down="blurInBottom" data-scrolly-mouseover="zoomIn"> 
     I am animate when you hover me 
</div>
```

**Mouse Out Animtion:** Add `data-scrolly-mouseout="fadeInLeft"` attribute to animate on mouse out event.
``` html
<div data-scrolly-down="blurInBottom" data-scrolly-mouseout="fadeInLeft"> 
     I am animate when you click me 
</div
```

**Targeted Object Animate When You Click:** Targeted Object Animate When You Click: If you want to animate a content by clicking by another one, follow this simple instruction. 
``` html
<input type="button" value="Hit me to Animate targetd object" data-srolly-selector="targetElement">

<div data-scrolly-selector="targetElement" data-scrolly-target-click="pushReleaseFromBottom">
     I am animate your target object when you click me
</div>
```

**Targeted Object Animate When You Mouse Over:** Animate any content while hovering mouse on another one.
``` html
<input type="button" value="Hit me to Animate targetd object" data-srolly-selector="targetElement">

<div data-scrolly-selector="targetElement" data-scrolly-target-click="flipYZoomIn">
     I am animate your target object when you hover me
</div>
```

**Targeted Object Animate When You Mouse Out:** Unlike those two follow the instruction below to animate targeted contents while doing mouse out on another one.
``` html
<input type="button" value="Hit me to Animate targetd object" data-srolly-selector="targetElement">

<div data-scrolly-selector="targetElement" data-scrolly-target-click="rotateInLeft">
     I am animate your target object when you mouse out from me
</div>
```

# Why Scrolly.js
Scrolly JS is efficient and flexible JavaScript library for building an interactive and attractive animation with scrolling. Fully responsive, lightweight, powerful and flexible pure JavaScript scroll animation library.

### Animated by CSS
Your imagination can be real. Just imagine and implement your own animation effect with this platform.

### Flexibility and extendibility
Easy-going installation and flexible scroll animation library that have insignificant production time. The platform is developer friendly and extendable.

### Support for responsive
This is 100% responsive and ready for all devices with any screen resolutions.

### Lightweight
Just a 12KB file which is really lightweight to use any of your projects.

### Easy to use
A Very easiest scroll animation library which has extensive features to build any scroll animation as you want.

### No dependency
Plug and play and ready to implement. No dependency with any third party JavaScript plugin, framework or library.
