##Your First Web Page

###Let's just start with plain text
For now, we'll start with just a text file that will tell people a little about you, a school club or a hobby you like. We'll put this in our code editor even though we are just doing text.

Let's get going by starting up Visual Studio Code. Once the editor is open, we will want to start a new folder for all of our work. Start by clicking "File" (1) and then "Open folder..." (2)

![VSCode File Open Folder](images/vscode-file-open-folder.png?raw=true)

In the dialog window that comes up, navigate to a good location to store your new project. Often the best place will be your "Documents" folder, but choose a location where you will remember where to find it later. Once you have a location selected, you will want to create a new folder for your web pages. Click on the "New Folder" (1) Change the name of the new folder to something you like (2) and then Click the "Select Folder" button at the bottom (3)

![VSCode New Folder](images/vscode-new-folder.png?raw=true)

When you return to Code, you should have your new website folder open in your project.

![Code Folder](images/code-folder.png?raw=true)

Now let's create a new file in your website folder for the text of our web page. We'll do this by hovering the mouse over the folder name and clicking the icon that looks like a piece of paper with a plus sign (1).

![New file](images/new-file.png?raw=true)

Name the file "index.html". Really, you could call the page anything, but most websites have an index page as their first page, so it's a good idea to name your file this way.

It's time to add some text to this file. Add the following text to your page. You could add your own text, but this is the text we will be referring to for the rest of this tutorial.

````Text
Visit Anytown, USA!

Things to Do
Hiking
Biking
Horseback
Backpacking

Amazing Museums
While most museums are a collection of old artifacts and stuff that no one is really interested in seeing, our musuems are the best of the best.
You won't find anything like these any where else in the world. Our museums rival that of our closest competitors including the Museum of Bad Art, the Paris Sewers Musuem and the Museum of Broken Relationships.
Come check them out...the fun is waiting for you.
 
SplashAnyone Waterpark
Our waterpark is the biggest and best park in the Western World. Just south of interstate 2015, you'll find a sweet mix of Super Slides and lazy rivers.
If that wasn't enough, we have 376 of the best food trucks in the state serving everything from fried gummy bears to lemonade and pizza. Don't forget if you buy our collectors edition souvenir water park keepsake, you get free refills all year.
And we wouldn't be SplashAnyone without the rules about splashing ... wait there are no rules.

Best Zoo in Town
Finally, you won't want to miss out cuddly little zoo animals. Lions, tigers and bears...Oh My! We have the largest selection of born in captivity animals. We didn't want to take the from their natural habitat, so we just got them from the other zoos in the state.

How to Get Here
By Plane
By Train
By Automobile
By Boat

````

Save your work by clicking on the File and then Save. You could also use the keyboard shortcut CTRL+S or Command+S to save your work.

So far, all we have is a little text. If we were double-click the file to open it in a browser (go ahead and try it if you want to) you would see something like this.

![Plain Text](images/plain-text.png?raw=true)

###Let's Add Some Formatting

So we have plain text and it doesn't look very nice right now in the browser. That's because the browser was made for HTML or Hyper Text Markup Language. This is just a way to put extra text in our plain text that tells the browser program how it should show our data...that the Markup. The Hyper Text was a method developed for creating and linking content where the reader can jump to other related content quickly.

Were are going to start with just giving our text a way to look formatted a little nicer in the browser. We'll add some of the linked content in the later modules for Choose to Code.

First, let's tell the browser that the document that we are working with is going to be an HTML document. We'll do that by putting the following code at the beginning of our file.

<!-- mark:1 -->
````HTML
<!doctype html>
Visit Anytown, USA!

Things to Do
Hiking
...
````

Most browsers will assume that it is HTML without this, but it's never a bad idea to set the expectation for the browser to view your file as HTML.

Next, we need to tell the browser where the HTML starts and stops. We do this by using tags. Opening tags look like this "\<html>" and closing tags look like this "\</html>". Let's put these at the top and bottom of your web page now.

<!-- mark:2,12 -->
````HTML
<!doctype html>
<html>
Visit Anytown, USA!

Things to Do
Hiking

...

By Automobile
By Boat
</html>
````

There are two parts of an HTML page. There is the \<head> which has some information that is descriptive of your page and then the \<body>. The \<body> is the content of your page and how it should be displayed.

Let's add those tags now. We don't have any \<head> content just yet, so we will just put in a blank set of tags. We'll come back and add more interesting stuff in a minute. The rest of the content we will surround with the \<body> tags.

<!-- mark:3,4,11 -->
````HTML
<!doctype html>
<html>
	<head></head>
	<body>
	Visit Anytown, USA!

	Things to Do
	...
	By Automobile
	By Boat
	</body>
</html>
````

Next, we want to set a number of the lines to be "header" lines. We do this with tags \<h1>, \<h2>, and so on to \<h6>. The top most level is \<h1>. While we are at it, we want to mark the paragraphs of text with a \<p> tag. This helps the browser to format these as individual paragraphs rather than creating one long block of text.

<!-- mark: 5,12-23 -->
````HTML
<!doctype html>
<html>
	<head></head>
	<body>
	<h1>Visit Anytown, USA!</h1> 
	Things to Do 
	Hiking 
	Biking 
	Horseback 
	Backpacking

	<h2>Amazing Museums</h2>
	<p>While most museums are a collection of old artifacts and stuff that no one is really interested in seeing, our musuems are the best of the best.</p>
	<p>You won't find anything like these any where else in the world. Our museums rival that of our closest competitors including the Museum of Bad Art, the Paris Sewers Musuem and the Museum of Broken Relationships.</p>
	<p>Come check them out...the fun is waiting for you.</p>

	<h2>SplashAnyone Waterpark</h2>
	<p>Our waterpark is the biggest and best park in the Western World. Just south of interstate 2015, you'll find a sweet mix of Super Slides and lazy rivers.</p>
	<p>If that wasn't enough, we have 376 of the best food trucks in the state serving everything from fried gummy bears to lemonade and pizza. Don't forget if you buy our collectors edition souvenir water park keepsake, you get free refills all year.</p>
	<p>And we wouldn't be SplashAnyone without the rules about splashing ... wait there are no rules.</p>

	<h2>Best Zoo in Town</h2>
	<p>Finally, you won't want to miss out cuddly little zoo animals. Lions, tigers and bears...Oh My! We have the largest selection of born in captivity animals. We didn't want to take the from their natural habitat, so we just got them from the other zoos in the state.</p>

	How to Get Here 
	By Plane 
	By Train 
	By Automobile 
	By Boat
</body>

</html>
````

Save your work and open your file in a browser now, it should look much nicer.

![H1 and P tags](images/h1-and-p-tags.png?raw=true)

###Adding the Lists
Finally, we have two lists we want to work with. In HTML, we have two types of lists: Ordered and Unordered. An ordered list puts a numeric value at the beginning of each list item where unordered lists use a graphic symbol to mark each list item.

To create an ordered list, we use an \<ol> tag and for an unordered list, we use an \<ul> tag. For both lists, each individual list item is marked with an \<li> tag.

````HTML
	<h2>Things to Do<h2> 
	<ul>
		<li>Hiking</li>
		<li>Biking</li>
		<li>Horseback</li>
		<li>Backpacking</li>
	</ul>
````

````HTML
	<h2>How to Get Here</h2>
	<ol>
		<li>By Plane</li>
		<li>By Train</li>
		<li>By Automobile</li>
		<li>By Boat</li>
	</ol>
````

###Let's give your page a title
Remember that \<head> tag we put in early on. Let's go back and add another tag to tell your browser what to display in the window or tab title. This will help us know which window is your web page.

This time we are going to insert a \<title> tag to the \<head>. There are other things we can put in the \<head> tag, but for now this is all we are going to do.

<!-- mark:4 -->
````HTML
	<head>
		<title>My First Web Page</title>
	</head>
````

Finally, save your work and open the page in a browser.

Congratulations, you turned a simple text file into an HTML file. You are now ready to move on and learn how to add some more style and flair to your web page.