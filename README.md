alternating-image-layout
========================

A Simple CSS include and style classes allows you to setup a page layout similar to Apple's product description pages where the product image and product description placement is alternated between left and right columns for every row. Check out the demo at: http://thomasyung.com/alternating-image-layout

Usage:
------

Include this snippet in your html head:
```html
<pre>
<link rel="stylesheet" type="text/css" href="alternating-image-layout.css">
</pre>
```

Take a look at the index.html file to see how to format your HTML divs. Essentially, you need several div containers with our custom classes wrapped around the content you wish to display.

The first level div uses this class as a wrapper: 
*.alternating-layout-container*

To separate each row content semantically, we add a hr before/after each row. If you don't add this, you will not get your images to alternate. The fix would be to go into the CSS and change the code references from :nth-child(2n) to :nth-child(even) and from :nth-child(4n) to :nth-child(odd). I suggest keeping the hr to separate the rows, because it will read better for users who browse the web on browsers that don't support the latest CSS standards. eg. Lynx ;-)

The second level div defines the rows: 
*.alternating-layout-row*

The third level div defines the columns: 
*.alternating-layout-img*
*.alternating-layout-desc*

I chose to display the image before the description. However, you can switch it around if you choose.

The images inside the *.alternating-layout-img* container will resize itself to fit the columns as they get bigger/smaller.

If you don't agree with the media query breakpoints that I used, go ahead and change them.