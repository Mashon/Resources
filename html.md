Create a folder to store your html and css files in.

Create homepage.html and open in atom.

In atom type `html<tab>` and it should auto fill the Doctype information at the top.  

Give the webpage a title: Newsletter


Create two new files: `mstyle.css` and `normalize.css`.
Place the links to those stylesheets in the head section of your html.

```html
<link type="text/css" rel="stylesheet" href="normalize.css">
<link type="text/css" rel="stylesheet" href="mystyle.css">
```

Remember that the stylesheets are read from top to bottom so we want the `normalize.css` file to be read first. This ensurest that it is resetting our webpage to display the same across all browsers.  Then our additional styling will be read from the `mystyle.css` file.

From the link [here](https://necolas.github.io/normalize.css/) download the normalize file and copy in the normalize.css stylesheet.

Now, were ready to get started laying out the structure of our html page.  

We know that we need a header and footer so we can go ahead and create those elements:

```html
<header>
</header>

<footer>
</footer>
```
I need a title on my page so I'll go ahead and create one between the header and footer elements.

```html
<div class="month_title">
<h1>December</h1>
<div>
```

I'll also need content to go in the main body of the newsletter so i'll include that below the title using a <section> tag.

```html
<section class="main-article">
</section>
```
I want a space for events as well so those will go inside another section.
```html
<section class="events">
</section>
```
My entire body section now looks like this:

```html
  <body>
    <header>
    </header>

    <div class="month_title">
    <h1>December</h1>
    <div>

    <section class="main-article">
    </section>

    <section class="events">
    </section>

    <footer>
    </footer>
      
  </body>
  ```

Rememberthat its important to start adding well thought out class names while your creating your html structure. This allows you to differentiate tags from each other, like our two section elements on the page. It also prepares you for the styles you'll add later with css.

Now lets progress down the page from top to bottom.

We start with our header. This will contain the main navigation links for the site.

Place the following code inside the header tags.

```html
      <nav>
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">Past Issues</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
      </nav>
```

`<nav></nav>` tags are used to define sections that will contain main navigation links for a site.  
Links are typically stored in unordered lists. The <ul></ul> tags delineate the start end of a list and the <li></li> tags showthe beginning and end of each item in that list.

Links themselves begin and end with <a></a> tags and are *nested inside* the <li></li> tags. Remember, nested tags must be closed in order!

Finally notice the `<a href="#">` portion of the link. This is called a stub and is used as a placeholder when you have not yet specified where the page should link to. 

We have a title set up for the main page, "December" but we're also going to need an article title for the main article of our site. 
```html
  <section class="main-article">
      <h3>Welcome Bob Smith - CTO</h3>
  </section>
```

We also need some content so lets add some <p></p> tags. 

```html
 <section class="main-article">
      <h3>Welcome Bob Smith - CTO</h3>
      <p></p>
      <p></p>
      <p></p>
      <p></p>
      <p></p>
  </section>

```
Grap some filler [text](www.hipsum.co) and place that in the paragraph tags.

The next section contains events and for each event we want to have an image with some text below it.  

In order for the text below each iamge to be "attached" below it, it would make sense that these two things are attached. To do this we can place in the same container <div></div>

```html
    <div class="each_event">
        <img src="http://placehold.it/350x150"/>
        <p>Echo park kogi thundercats, vice vinyl sustainable 3 wolf moon plaid cornhole marfa 90's helvetica migas humblebrag. Next          level wolf +1 umami.</p>
    </div>
```

Here we are creating a <div></div> which holds and image and paragraph inside it.

You can use an image on your computer, from the internet or a [placeholder](https://placehold.it/).

Make two more divs, both with the same `"each-event" class and place an image and a short paragraph inside each of them.

Thats enough in our body for now so lets go ahead and finish out our layout with the footer.

Our footer is going to contain the same navigation links as our header and some social media links.

First, put the same information in the <nav></nav> links in the header into the footer section.

Now we'll add social media icons from [Font Awesome](https://fortawesome.github.io/Font-Awesome/). There are over 600 free icons which act just like fonts so you can change their color or size using the same css you would use to change text.

In the getting started section of the site follow the steps in the *EASIEST: BootstrapCDN by MaxCDN* section. ??? Make sure to place the link *above* your other stylesheets ????

Now lets add the twitter icon and link it to Twitter. Add the code below right under your "Contact" link.

```html
    <li><a href="https://twitter.com"><i class="fa fa-twitter"></i></a></li>
```

Notice that because the icon is what we want to display for the link, it is nested *inside* of the anchor tag.

Add two more icons linking to Facebook and Instagram.

*********************************************************************************** 
