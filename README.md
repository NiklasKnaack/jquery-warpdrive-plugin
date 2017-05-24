# Warp drive jQuery plugin
(jquery-warpdrive-plugin)

## Preview

![Alt text](https://cloud.githubusercontent.com/assets/10435486/26393070/052133f0-4069-11e7-8f6b-1d6f79cfcd12.gif "Preview")

## Description

Warp drive is a lightweight jQuery plugin that helps you create a cool, interactive, configurable, HTML5 canvas based warp drive/starfield effect. 

## Demos & Examples

### Overview & Examples

* <http://blog.niklasknaack.de/2017/05/warp-drive-jquery-plugin.html>

### CodePen Demo (old version)

* <https://codepen.io/NiklasKnaack/pen/OmwgKb>

### More Examples

* <http://nkunited.de/jquery/plugins/warpdrive/example1.html>
* <http://nkunited.de/jquery/plugins/warpdrive/example2.html>
* <http://nkunited.de/jquery/plugins/warpdrive/example3.html>
* <http://nkunited.de/jquery/plugins/warpdrive/example4.html>
* <http://nkunited.de/jquery/plugins/warpdrive/example5.html>
* <http://nkunited.de/jquery/plugins/warpdrive/example6.html>
* <http://nkunited.de/jquery/plugins/warpdrive/example7.html>
* <http://nkunited.de/jquery/plugins/warpdrive/example8.html>

### Showcase

* <http://blog.niklasknaack.de/?header=WarpDrive>

## Installation

Coming soon.

## Example Usage

### jQuery

```js
$( '#holder' ).warpDrive();
```

### jQuery with parameters:

```js
var settings = {

    width: 480,/*width*/
    height: 480,/*height*/
    autoResize: false,/*enable/disable autoResize*/
    autoResizeMinWidth: null,/*set autoResize min width*/
    autoResizeMaxWidth: null,/*set autoResize max width*/
    autoResizeMinHeight: null,/*set autoResize min height*/
    autoResizeMaxHeight: null,/*set autoResize max height*/
    addMouseControls: true,/*enable/disable mouse controls*/
    addTouchControls: true,/*enable/disable touch controls*/
    hideContextMenu: true,/*enable/disable canvas context menu*/
    starCount: 6666,/*count of active/moving stars*/
    starBgCount: 2222,/*count of inactive/background stars*/
    starBgColor: { r:255, g:255, b:255 },/*background stars color*/
    starBgColorRangeMin: 10,/*background stars color range min of starBgColor*/
    starBgColorRangeMax: 40,/*background stars color range max of starBgColor*/
    starColor: { r:255, g:255, b:255 },/*stars color*/
    starColorRangeMin: 10,/*stars color range min of starBgColor*/
    starColorRangeMax: 100,/*stars color range max of starBgColor*/
    starfieldBackgroundColor: { r:0, g:0, b:0 },/*background color*/
    starDirection: 1,/*stars moving in which direction*/
    starSpeed: 20,/*stars moving speed*/
    starSpeedMax: 200,/*stars moving speed max*/
    starSpeedAnimationDuration: 2,/*time in seconds from starSpeed to starSpeedMax*/
    starFov: 300,/*field of view*/
    starFovMin: 200,/*field of view min*/
    starFovAnimationDuration: 2,/*time in seconds from starFov to starFovMin*/
    starRotationPermission: true,/*enable/disable rotation*/
    starRotationDirection: 1,/*rotation direction*/
    starRotationSpeed: 0.0,/*rotation speed*/
    starRotationSpeedMax: 1.0,/*rotation speed max*/
    starRotationAnimationDuration: 2,/*time in seconds from starRotationSpeed to starRotationSpeedMax*/
    starWarpLineLength: 2.0,/*line length*/
    starWarpTunnelDiameter: 100,/*tunnel diameter*/
    starFollowMouseSensitivity: 0.025,/*mouse follow sensitivity*/
    starFollowMouseXAxis: true,/*enable/disable mouse follow x axis*/
    starFollowMouseYAxis: true/*enable/disable mouse follow y axis*/

};

$( '#holder' ).warpDrive( settings );
```

### JS

```js
var warpdrive = new WarpDrive( document.getElementById( 'holder' ) );
```

### JS with parameters:

```js
var settings = {

    width: 480,/*width*/
    height: 480,/*height*/
    autoResize: false,/*enable/disable autoResize*/
    autoResizeMinWidth: null,/*set autoResize min width*/
    autoResizeMaxWidth: null,/*set autoResize max width*/
    autoResizeMinHeight: null,/*set autoResize min height*/
    autoResizeMaxHeight: null,/*set autoResize max height*/
    addMouseControls: true,/*enable/disable mouse controls*/
    addTouchControls: true,/*enable/disable touch controls*/
    hideContextMenu: true,/*enable/disable canvas context menu*/
    starCount: 6666,/*count of active/moving stars*/
    starBgCount: 2222,/*count of inactive/background stars*/
    starBgColor: { r:255, g:255, b:255 },/*background stars color*/
    starBgColorRangeMin: 10,/*background stars color range min of starBgColor*/
    starBgColorRangeMax: 40,/*background stars color range max of starBgColor*/
    starColor: { r:255, g:255, b:255 },/*stars color*/
    starColorRangeMin: 10,/*stars color range min of starBgColor*/
    starColorRangeMax: 100,/*stars color range max of starBgColor*/
    starfieldBackgroundColor: { r:0, g:0, b:0 },/*background color*/
    starDirection: 1,/*stars moving in which direction*/
    starSpeed: 20,/*stars moving speed*/
    starSpeedMax: 200,/*stars moving speed max*/
    starSpeedAnimationDuration: 2,/*time in seconds from starSpeed to starSpeedMax*/
    starFov: 300,/*field of view*/
    starFovMin: 200,/*field of view min*/
    starFovAnimationDuration: 2,/*time in seconds from starFov to starFovMin*/
    starRotationPermission: true,/*enable/disable rotation*/
    starRotationDirection: 1,/*rotation direction*/
    starRotationSpeed: 0.0,/*rotation speed*/
    starRotationSpeedMax: 1.0,/*rotation speed max*/
    starRotationAnimationDuration: 2,/*time in seconds from starRotationSpeed to starRotationSpeedMax*/
    starWarpLineLength: 2.0,/*line length*/
    starWarpTunnelDiameter: 100,/*tunnel diameter*/
    starFollowMouseSensitivity: 0.025,/*mouse follow sensitivity*/
    starFollowMouseXAxis: true,/*enable/disable mouse follow x axis*/
    starFollowMouseYAxis: true/*enable/disable mouse follow y axis*/

};

var warpdrive = new WarpDrive( document.getElementById( 'holder' ), settings );
```

### Color settings/valid formats for starColor, starBgColor & starfieldBackgroundColor

```js
starBgColor: { r:255, g:255, b:255 }
```
```js
starBgColor: '#ffffff'
```
```js
starBgColor: '#fff'
```
```js
starBgColor: 'rgb(255,255,255)'
```

### Pause/unpause

### jQuery

```js
$( '#holder' ).warpDrive( 'pause' );
$( '#holder' ).warpDrive( 'unpause' );
```

### JS

```js
warpdrive.pause();
warpdrive.unpause();
```

Pause/unpause example:
* <http://nkunited.de/jquery/plugins/warpdrive/example8.html>

## License

This plugin is available under [the MIT license](http://mths.be/mit).

## Author

_– [Niklas](http://niklasknaack.de/)_