# .FITRGRID

![fitrgrid logo](https://github.com/wachilt/Fitrgrid/blob/master/images/icons/retina.png)


## Mobile / small screen first responsive grid

Fitrgrid is a fork of [fitgrd](https://github.com/jayalai/fitgrd) - the lightweight responsive grid by Jan Müller, and inherits all features of the original.  

Fitrgrid is divided into twelve percentage-based columns. Each column has a two percent gutter. Fitrgrid comes with a single media query (for viewports wider than 640px) that you can adjust or supplement to taste.

#### [Fitrgrid demo](http://wachilt.github.io/Fitrgrid)

##  How does Fitrgrid differ from fitgrd?  
I've worked with the original fitgrd and love it's simplicity. However, I now take a mobile-first approach to web development and wanted fitgrd to match these principles. I dismantled and reconfigured fitgrd as the new mobile-first Fitrgrid.

Fitrgrid has been (re)built from the ground up for small screen first web development and adds a new extra-wide grid option. Fitrgrid CSS weighs in at the same 4KB (uncompressed) file size of the original project and works well with modern mobile and desktop browsers - some older ones too.

##  Why not use Flexbox?
I use Flexbox. I've also been experimenting with [Grid](https://drafts.csswg.org/css-grid/).  
I don't subscribe to a one-size-fits-all philosophy, and for the moment I don't believe that a single layout technology is the solution to absolutely every web development scenario.

The Flex spec isn't finalised yet and there are still [Flexbugs](https://github.com/philipwalton/flexbugs). I also need to provide some clients with older browser compatibility. I therefore have a choice of sticking with a tried and tested grid system or using Flexbox coupled with a compensatory polyfill. I don't like throwing JS at every problem either.

In this respect I still find a 'traditional' grid system preferable to Flexbox in certain circumstances. This will undoubtedly change in the near future, especially as I plan to add Flex functionality to Fitrgrid.

##  Basic Setup 
To add Fitrgrid to your website, simply include `fitrgrid.pack.css` into your document's `<head>`

To guarantee a perfect responsive grid, follow these specs:

- container (`header`, `div`, `article`, `footer` etc.)
	- class center
		- class row
			- classes fg1 - fg12 as required
			
			
##  Markup example
````html
<header>
	<div class="center">
		<div class="row">
			<section class="fg2">
				your logo
			</section>
			<section class="fg10">
				page navigation would go here
			</section>
		</div>
	</div>
</header>

<article class="your-class-name">
	<div class="center">
		<div class="row">
			<section class="fg4"> lorem ipsum ... </section>
			<section class="fg4"> lorem ipsum ... </section>
			<section class="fg4"> lorem ipsum ... </section>		
		</div>
	</div>
</article>

<footer>
	<div class="center">
		<div class="row">
			<section class="fg6"> footer copyright </section>
			<section class="fg6"> footer navigation </section>
		</div>
	</div>
</footer>

````

##  Utility classes
For the moment Fitrgrid keeps it simple with just 4 utility classes:

| Utility class      | Description
| -----------|---
| .fg-no-gutter | Perfect for big edgeless image grids
| .fg-no-mobile | Do not display content on small screen devices
| .fg-no-desktop | Do not display content on large screen devices
| .fg-wide _(new!)_ | Full-width edgeless grids constrained by .center class width (default 1280px)

Fitrgrid will feature additional utility classes in future.

##  Compatibility  
Fitrgrid works well in all HTML5 compatible web browsers.

Add Modernizr and Fitrgrid should work all the way back to (dare I even utter it) IE7.

##  Acknowledgement 
A special thank you to Jan Müller for the original fitgrd project and for being so open and friendly. :)
