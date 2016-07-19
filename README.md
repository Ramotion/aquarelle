# Aquarelle
[![Bower](https://img.shields.io/bower/v/aquarelle.svg)]()
[![Twitter](https://img.shields.io/badge/Twitter-@Ramotion-blue.svg?style=flat)](http://twitter.com/Ramotion)
[![Travis](https://img.shields.io/travis/Ramotion/animated-tab-bar.svg)](https://travis-ci.org/Ramotion/aquarelle)


[shot on dribbble:](https://dribbble.com/shots/2781510-Web-Transition-Effect)
![preview](./Screenshots/web__transition__effect_ramotion.gif)

## Browser support

* Chrome
* Safari
* Opera
* Firefox
* IE 11

## Installation

`bower install aquarelle`

Then insert in your html:

```html
<script src="bower_components/three.js/build/three.js"></script>

<script src="bower_components/aquarelle/Aquarelle.js"></script>

<script src="bower_components/three.js/examples/js/postprocessing/EffectComposer.js"></script>

<script src="bower_components/three.js/examples/js/postprocessing/ClearPass.js"></script>
<script src="bower_components/aquarelle/AquarellePass.js"></script>
<script src="bower_components/three.js/examples/js/postprocessing/ShaderPass.js"></script>
<script src="bower_components/three.js/examples/js/shaders/CopyShader.js"></script>

<script src="https://bl.ocks.org/mbostock/raw/4241134/d3.geom.contour.min.js"></script>
```


## API

### Constructor

`new Aquarelle(textureImage, maskImage[, options]);`

| Names | Required | Type | Description
| --- | --- | --- | ---
| textureImage | `true` | `string`, `Image` or `<img>` | background image
| maskImage | `true` | `string`, `Image` or `<img>` | background image mask
| options | `false` | `object` | initial options

### Options

| Names | Defaults | Description
| --- | --- | ---
| fromAmplitude | `50` | initial noise amplitude value
| toAmplitude | `0` | final noise amplitude value
| fromFrequency | `8` | initial noise frequiency
| toFrequency | `7` | final noise frequiency
| fromOffset | `-30` | initial mask size
| autoplay | `false` | `true` - start animation before first frame is being rendered
| loop | `false` | `true` - repeat animation in loop
| duration | `8000` | animation duration

### Events

| Names | Description
| --- | ---
| created | triggered before first frame is rendered
| changed | triggered before rendering of a frame
| completed | triggered before latest frame is rendered
| started | triggered before animation is started
| played | triggered after animation is started
| paused | triggered before pause of animation
| stopped | triggered before reset of animation

### Methods

| Names | Description
| --- | ---
| `pause()` | pause animation
| `play()` | start animation
| `stop()` | stop and reset animation
| `start()` | start animation over
| `reverse()` | reverse animation
| `reset()` | re-render frame
| `setOptions([object])` | set animation options
| `transitionInRange(startValue, endValue[, startTimeMS[, endTimeMS]])` | return value between `startValue`..`endValue` in range `startTimeMS`..`endTimeMS`
| `addEventListener(type, listener)` | add listener (`listener`) of event (`type`)
| `removeEventListener(type, listener)` | remove (`listener`) of event (`type`)


## Usage

##### Initialization

```javascript
var aquarelle = new Aquarelle(textureImage, maskImage[, options]);
```

##### Listeners

```javascript
function listener(event) {}

aquarelle.addEventListener('created', listener);

aquarelle.removeEventListener('created', listener);
```


## Licence

Aquarelle is released under the MIT license.
See [LICENSE](./LICENSE) for details.


## About
This project is maintained by [app development agency](https://ramotion.com?utm_source=gthb&utm_medium=special&utm_campaign=aquarelle) [Ramotion Inc.](https://ramotion.com?utm_source=gthb&utm_medium=special&utm_campaign=aquarelle)
See our other [open-source projects](https://github.com/ramotion) or [hire](https://ramotion.com?utm_source=gthb&utm_medium=special&utm_campaign=aquarelle) us to design, develop, and grow your product.
