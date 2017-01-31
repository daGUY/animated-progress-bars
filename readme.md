# Animated Progress Bars
* By James Scariati
* May 2015

## Description
Add a subtle "barbershop pole" stripe animation to progress bars. Gracefully degrades in older browsers that don't support CSS3 animation and/or linear gradients (the stripes will appear without movement, or not appear at all).

**[View Demo](http://scariati.kissr.com/github/apb/)**

## Dependencies
* [jQuery](http://jquery.com)
* [Velocity](http://julian.com/research/velocity/)

## Use
Include jQuery, Velocity, the `jquery.progressBar.js` plugin, and `jquery.progressBar.css` in your HTML:

```html
<head>
	<link rel="stylesheet" href="css/jquery.progressBar.css" />
	<script src="lib/jquery.min.js"></script>
	<script src="lib/jquery.progressBar.js"></script>
	<script src="lib/velocity.min.js"></script>
</head>
```

Next, add an element to your HTML with the following structure:

```html
<div class="progress" data-step="1" data-total="5"></div>
```

The `data-step` and `data-total` attributes are used to determine how much to fill the progress bar. In this example, `1 / 5 = 0.2`, so the progress bar will fill to 20%.

Then call the plugin on your element:

```javascript
$(".progress").progressBar();
```

## Options
The following options are available:

```javascript
$(".progress").progressBar({
	animateFill: true,
	animateStriping: true,
	fillColor: "#ccc",
	fillGradient: true,
	showPercentage: true,
	showStriping: true,
	trackColor: "#a2a4a6",
	width: "100%"
});
```

* `animateFill`: animates the progress bar's fill from zero. Defaults to `true`
* `animateStriping`: animates the striping on the progress bar. Defaults to `true`
* `fillColor`: sets the color of the progress bar's fill. Accepts any valid CSS color (hexcode, color keyword, etc.). Defaults to `#ccc`
* `fillGradient`: adds a gradient effect to the progress bar's fill. Defaults to `true`
* `showPercentage`: displays text above the progress bar showing the value it's filled to. Defaults to `true`
* `showStriping`: overlays a striping effect on the progress bar's fill. If this is `false`, `animateStriping` has no effect. Defaults to `true`
* `trackColor`: sets the color of the track that the progress bar fills. Defaults to `#a2a4a6`
* `width`: width of the progress bar. Defaults to `100%`