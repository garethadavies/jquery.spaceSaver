# jQuery.spaceSaver

A simple show more/show less plugin. For when less is more.

This plugin has been designed to work with my own system, but feel free to hack it to death if required.

Current version: **0.1.0**

## Requirements

* jQuery (1.9.1+) - http://jquery.com

## Getting up and running

### Download the files

* [jquery.spaceSaver.js](https://github.com/garethadavies/jquery.spaceSaver/raw/master/jquery.spaceSaver.js)
* [jquery.spaceSaver.css](https://github.com/garethadavies/jquery.spaceSaver/raw/master/jquery.spaceSaver.css)

### Reference the files

```html
<link rel="stylesheet" href="path/to/file/jquery.spaceSaver.css" type="text/css">
```

This script requires jQuery so make sure you add the space saver script after it or define jQuery as a dependency.

```html
<script src="path/to/file/jquery.spaceSaver.js"></script>
```

#### Optional

If you wish space saver to react to window resizes, you will need to include [jquery.debouncedresize.js](https://github.com/louisremi/jquery-smartresize) before the space saver script or define it as a dependency.

This feature is set to false by default, but can be enabled by passing ```resizeable: true``` during initialisation.

### Usage:

#### HTML

This plugin required a container for the content you wish to show more/show less. You will need to add the 'space-saver' class to the container, so it has the required styling.

```html
<div id="container" class="space-saver">
	<p>Some content here</p>
</div>
```

#### JS

```js
$('#container').spaceSaver({
	// This height will be where the contents of the target div is cut-off and replaced by the 'show more'. 
	// You can adjust this to suit your content
	heightLimit: 100,
	// The background colour (Hex) of the 'show more/show less'
  	backgroundColor: '#fff',
  	// You can supply the html for including an 'open' icon
  	iconOpen: '<i class="icon-up-open"></i>',
  	// You can supply the html for including an 'closed' icon
  	iconClosed: '<i class="icon-down-open"></i>',
  	// You can set whether you want the plugin to refresh if the window is resized.
	// This requires jquery.debouncedresize.js to be available
  	resizable: false
});
```

**NOTE:** The DOM must be rendered before you initialise the plugin so that it can access the element's height.
