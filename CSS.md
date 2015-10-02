##Let’s add some style with Cascading Style Sheets (CSS)

###Add some elements to the page

Before we take a look at adding some style to our page, let's add a few more tags to our web page. While you can make everything in your web page with the \<h1> and \<p> tags for headers and paragraphs, it it helpful to have some other items in your page. Some of these items will be more informative about the text that is inside of the tag.

In HTML5 we have a number of element tags that actually describe the content that we have on the page better. For example, instead of just having an \<h1> tag, we can add a \<header> tag to be clear that this is a header for the document or a section. Similarly, we can also set a \<footer> for the bottom of the document or section.

Let's add a header to the top of your "index.html" page. Here we added a \<header> tag around our \<h1> tag.

<!-- mark: 2,4 -->
```html
<body>
	<header>
		<h1>Visit Anytown, USA!</h1>
	</header>
```

Many web pages will use a footer to include contact information as well as a Copyright for the information on the page. Let's add one now.

<!-- mark: 1,3 -->
```html
	<footer>
		Copyright 2015
	</footer>
</body>
</html>
```

Save your work and then refresh "index.html" in your broswer to see the updates that you made to the header and footer. At this point, you might not notice any change. That will come when we start adding some styles.

###Adding Images
Now, for a little visual appeal, we want to add some images to our text. Usually, these images will be in a folder on your website, but they could really come from anywhere as long as you know the URL.

Let's create a folder for images and then link an image to your web page.

![images folder](images/images-folder.png?raw=true)

Next, copy an image to this folder and then we can add it to part of your web page with an \<img> tag. Notice that the "src" attribute is pointing to where the image is stored. The second example below shows an image located on another server.

<!-- mark: 1 -->
```html
EXAMPLES:
<img src="images/picture1.jpg" />

<img src="http://someotherserver.com/image.jpg" />
```

Let's add some images to our HTML to make our page look more complete. We're going to use sample images from the LoremPixel.com website in our page.

Near the beginning of each \<article> just after the closing \</h2> tag, we want to add an \<image> tag to give our content a little visual appeal.

<!-- mark: 3,10,17 -->
```html
<article>
	<h2>Amazing Museums</h2>
	<img src="http://lorempixel.com/200/100/city/1" />
	<p>
	...
	</p>
</article>
<article>
	<h2>SplashAnyone Waterpark</h2>
	<img src="http://lorempixel.com/200/100/city/2" />
	<p>
	...
	</p>
</article>
<article>
	<h2>Best Zoo in Town</h2>
	<img src="http://lorempixel.com/200/100/city/3" />
	<p>
	...
	</p>
</article>
```

Save your work and then refresh "index.html" in your broswer to see the pictures that you have added to each of the articles.

###Adding Hyperlinks
Finally, let's learn how to add links to other locations. We will use an anchor tag for this, and we'll start with something simple like text. Let's take our list of things to do and make hyperlinks to a search engine.

<!-- mark: 3 - 6 -->
```html
<h2>Things to Do</h2>
<ul>
	<li><a href="http://www.bing.com/search?q=hiking">Hiking</a></li>
	<li><a href="http://www.bing.com/search?q=biking">Biking</a></li>
	<li><a href="http://www.bing.com/search?q=horseback">Horseback</a></li>
	<li><a href="http://www.bing.com/search?q=backpacking">Backpacking</a></li>
</ul>
```

Save your work and then refresh "index.html" in your broswer to see the items in the "Things to Do" list are now hyperlinks. When you click on one of the links, you will be taken to the page at the URL in the "href" attribute of the \<a> tag.

Not only can links be made with text, but you can also change hyperlinks to a more interesting link like an image by changing the content of the anchor tag (\<a>). For example, in the following hyperlink, if you had a Microsoft logo in your images folder,  you could replace the text of your link with that image. There is no text displayed as part of this hyperlink.

```html
<a href="http://microsoft.com"><img src="images/microsoftlogo.jpg" /></a>
```

###Now for some style
Now that you have added a few more items to work with in your HTML, let's look at some ways that we can make things look a little more stylish than plain black and white text.

We have already seen that using different tags will make items display in different sizes, but we can also use what are called styles. There are two different ways we can do styles. The first is with inline styles where we add a description of how we want the text to appear in the middle of our HTML.

```html
<p style="color:red;text-align:center">some text</p>
```

The problem with inline styles like the example above is that if you have a lot of paragraphs on your page and you want them to all look this way, you would have to put this style on each paragraph. When you want to change all the paragraphs that are red throughout my website...there's potentially a lot of work to do.

So we turn the second (and preferred) method of linking a stylesheet to our page. This stylesheet tells how to render items in our web page and applies it consistently across all items. The way we determine how the styles are applied are based on "selectors" or selection criteria. Additionally, we can have multiple stylesheets loaded and they will add all of their styles collectively. This is why they are called "Cascading Style Sheets" (which is why they have an extension ".css")

In the example below, we are loading a stylesheet called "app.css" that will contain our web page specific styles.

<!-- mark: 3 -->
```html
<head>
	<title>My First Web Page</title>
    <link href="app.css" rel="stylesheet"/>
</head>
```

Let's do that now with your existing "index.html" page we have already created. First create a new file called "app.css" in the same folder as your index.html file and add the above \<link> to the stylesheet.

![Add app css](images/add-app-css.png?raw=true)

Now it's time to add some flair to your web page. First, let's change the look of our header and footers that we created. For this, we are going to use the tag selectors for \<header> and \<footer>.

```CSS
header, footer {
	background-color: #004a4a;
	color: #ddd;
}
```

Notice that we just use the tag name and then we have a list of style attributes we want to set. We are going to use the "background-color" attribute. In order to set the color, we can use a color name like "red" or we can use a color value. To use a color value, you start with a hash symbol and then specify three values for red, green and blue. These values go from 00 through FF. We call these a hex value (short for hexadecimal...or a number system with 16 values...0-9 and A, B, C, D, E and F). So "#000000" will be 0 for Red, 0 for Green and 0 for Blue...or the color black. Sometimes you might see this short cut to just three numbers like "#ddd" which is the same as "#dddddd".

The example here is a dark teal and the text color is a lighter grey. Notice that in Visual Studio Code, you get a preview of the color when you are editing the stylesheet.

Save your "index.html" and "app.css" files and reload the index.html in your browser. Your header and footer should now be updated to the new color.

Now let's add some visual space around our text with some "padding". It might also look nice to center our text so let's go ahead and add that too.

<!-- mark: 4,5 -->
```CSS
header, footer {
	background-color: #004a4a;
	color: #ddd;
	padding: 20px;
	text-align: center;
}
```

Save your "app.css" and reload your "index.html" file in your browser. Notice that your content is now centered and has a little more room around the sides.

Let's move on to the body of the web page. Return to the "index.html" file and find the "Things To Do" list. Let's take the list that we have and put the HTML tag \<aside> around it to show they are not a main part of the content.

<!-- mark: 1, 9 -->
```html
<aside>
	<h2>Things to Do</h2>
	<ul>
		<li><a href="http://www.bing.com/search?q=hiking">Hiking</a></li>
		<li><a href="http://www.bing.com/search?q=biking">Biking</a></li>
		<li><a href="http://www.bing.com/search?q=horseback">Horseback</a></li>
		<li><a href="http://www.bing.com/search?q=backpacking">Backpacking</a></li>
	</ul>
</aside>
```
Do the same thing with the second list as well.

<!-- mark: 1, 9 -->
```html
<aside>
	<h2>How to Get Here</h2>
	<ol>
		<li>By Plane</li>
		<li>By Train</li>
		<li>By Automobile</li>
		<li>By Boat</li>
	</ol>
</aside>
```

Finally, for the rest of the body in our "index.html" file, let's define this as a \<section>. All of the content between our two \<aside> lists will be surrounded by this \<section> tag.

<!-- mark: 4, 17 -->
```HTML
	<aside>
		...
	</aside>
	<section>
		<article>
			<h2>Amazing Museums</h2>
			...
		</article>
		<article>
			<h2>SplashAnyone Waterpark</h2>
			...
		</article>
		<article>
			<h2>Best Zoo in Town</h2>
			...
		</article>
	</section>
	<aside>
		...
	</aside>
```

Now, let's set the colors and alignment for our lists. Open the "app.css" file and add the following style for the **aside** selector: 

```CSS
aside {
	padding-top: 10px;
	font-weight: bold;
}
````

One more little change while we are here, let's change the text in the \<h2> tag to the color darkblue. Notice we are using a named color now, and not a Hex color.

```CSS
h2 {
	color: darkblue;
}
```
Now, save "app.css" and "index.html" and refresh your browser to see the formatting updates that we have made.

Wait a second...we have a problem! All of the \<h2> tags were updated to be the darkblue and that is not what we wanted. We only wanted our list titles to be darkblue.

One of the ways we can fix this is to change our selectors to be more specific. At this point, the selector is choosing all \<h2> tags. If we want to limit the selection, for example, the following selector would tell the style only to be applied to \<h2> tags inside of the \<aside> tag.

```CSS
aside h2 {
	color: darkblue;
}
```

Notice that in Visual Studio Code, you can hover over the selector to see how the style will be applied on the page.

Again, save your changes to "app.css" and "index.html" and refresh the page in your browser. Now, not all of the \<h2> tags are darkblue, only the ones that are part of your lists.

###Styling with Class
So far, we have only been making style changes with tag selectors in our CSS. Another way to do selectors is by adding a class attribute to our tag. 

Let's take a look at how we do this. Modify the "Things to Do" list by adding a class attribute and giving it a value of "title".

<!-- mark: 2 -->
```html
<aside>
	<h2 class="title">Things to Do</h2>
	<ul>
		<li><a href="http://www.bing.com/search?q=hiking">Hiking</a></li>
		<li><a href="http://www.bing.com/search?q=biking">Biking</a></li>
		<li><a href="http://www.bing.com/search?q=horseback">Horseback</a></li>
		<li><a href="http://www.bing.com/search?q=backpacking">Backpacking</a></li>
	</ul>
</aside>
```

Now, we can tell our stylesheet to apply the darkblue color not to the \<h2> tag, but to the "title" class. Notice in the selector, we are telling it to use a class by starting the with a dot.

Remove the `aside h2 { ... }` section of the stylesheet and replace it with the following:

```CSS
.title {
	color: darkblue;
}
```

Save the "app.css" and refresh your browser to see your list titles updated and nothing else on the page was affected.

We can mix and match selectors for tags and classes to get pretty specific about the items we are asking to style. There is one more selector we can use for a tag with a specific id (we use "#" instead of the "." dot). First you need to add an "id" attribute to your html tag.

Let's modify the unordered list of "How To Get Here" and give it an ID.

<!-- mark: 3 -->
```HTML
<aside>
	<h2>How to Get Here</h2>
	<ol id="orderedlist">
		<li>By Plane</li>
		<li>By Train</li>
		<li>By Automobile</li>
		<li>By Boat</li>
	</ol>
</aside>
````

Then add whatever styling elements that you needed to make it look right for your design. For now, we will make the color of the text darkgreen.

```CSS
#orderedlist {
	color: darkgreen;
}
````

There is WAY MORE to CSS than we have covered here. If you want to see the potential of CSS, you can take a look at http://csszengarden.com. This is a collection of pages that use the exact same HTML, but have a different stylesheet applied for each page. As you click through the different designs, you will see the creativity and design that can come alive with styles.

In the next few modules, we'll get you set up to publish your web page to the Internet using Micrsoft's hosting platform called Microsoft Azure.