#Navigataur.css
*A pure CSS responsive navigation menu*


##Demo
Live Demo: http://micjamking.github.com/Navigataur/

## Compiling
Navigataur ships with an SCSS version, as well as a CSS version compiled from the SCSS version. To compile the SCSS version on your machine, you need to have both [Ruby][1] &amp; [Sass][2] installed

##Usage
To use `navigataur.css`, reference the stylesheet in the `<head>` of your document (or you can place within your own stylesheet).

To work out of the box, you will need to make the following adjustments to your markup (classes can be changed in the stylesheet if you use something different):
* An outer `<div>` with a class of `header`
* An `input[type=checkbox]` with an ID of `toggle` and a `div` wrapping around a `label[for=toggle]` with a class of `toggle` and an `onclick` attribute just above your list menu.
* The label also requires two data attributes for displaying the menu open/close text, allowing for complete localisation.
* A list menu (either ul or ol) with a class of `menu`, followed by the closing `div`

``` html
<input type="checkbox" id="toggle">
<nav role="navigation">
	<label for="toggle" class="toggle" data-open="Main Menu" data-close="Close Menu" aria-hidden="true" onclick></label>
	<ul class="menu">
	  <li><a href="#">Google</a></li>
	  <li><a href="#">Facebook</a></li>
	  <li><a href="#">Youtube</a></li>
	  <li><a href="#">Twitter</a></li>
	</ul>
</nav>
```

That's it! Everything works out of the box with this setup. However, like any CSS plugin/snippet, you will probably want to stylize it to match your sites theme. I've separated all functional CSS from the presentational CSS so you can jump right in and change everything you need without breaking the plugin. Just edit as needed below the following CSS comment:

```
/*--------------------------------
 Presentation Styles (Editable)
---------------------------------*/
```

##Support
WebKit rendering engine makes up the vast majority of mobile browsers (iOS, Android, Nokia), so you can expect the same level of support for mobile browsing as you see in Chrome/Safari.

* Chrome 16.0+
* Safari 5.1+
* Firefox 4.0+
* Opera 12
* IE9*
* iOS 4.0+
* Android 2.3+

*Internet Explorer 8 and below do not support media queries. If you need support for legacy IE versions, you can use an [IE specific stylesheet][3] to provide some styling support.*


##Details
* This plugin was created in response to [Menutron][4], a jquery plugin for responsive navigation menus. While I believe Menutron is more functional, as it provides access to native picker controls on mobile devices, `<select>` controls are not very attractive. Navigataur.css is for those that want the same responsive capabilities, but with more control over the styling.
* If you have any suggestions, comments, or creative insults for my code, [add an issue][5] or [fork the repo][6].


##Copyright
[BSD license][7] Copyright (c) 2012 Mike King ([@micjamking][8])

[1]: https://www.ruby-lang.org/
[2]: http://www.sass-lang.com/
[3]: http://css-tricks.com/how-to-create-an-ie-only-stylesheet/
[4]: https://github.com/micjamking/Menutron
[5]: https://github.com/micjamking/Navigataur/issues/new
[6]: https://github.com/micjamking/Navigataur/fork_select
[7]: http://opensource.org/licenses/bsd-license.php
[8]: https://twitter.com/micjamking