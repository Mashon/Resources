Create a folder to store your html and css files in.  

Create `homepage.html` and open in atom.  

In atom type `html<tab>` and it should auto fill the Doctype information at the top.    

Give the webpage a title: Newsletter  


Create two new files: `mstyle.css` and `normalize.css`.  
Place the links to those stylesheets in the head section of your html.  

```html
<link type="text/css" rel="stylesheet" href="normalize.css">
<link type="text/css" rel="stylesheet" href="mystyle.css">
```

Remember that the stylesheets are read from top to bottom so we want the `normalize.css` file to be read first. This ensurest that it is resetting our webpage to display the same across all browsers.  Then our additional styling will be read from the `mystyle.css` file.  

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

I'll also need content to go in the main body of the newsletter so i'll include that below the title using a `<section></section` tag.  

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

Remember that its important to start adding class names while your creating your html structure. This allows you to differentiate tags from each other, like our two section elements on the page. It also prepares you for the styles you'll add later with css.  

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
Grap some filler [text](www.hipsum.co) and place it in the paragraph tags.  

The next section contains events and for each event we want to have an image with some text below it.  

In order for the text below each image to be "attached" below it, it would make sense that these two things are attached. To do this we can place in the same container div.  

```html
    <div class="each_event">
        <h5>Event 1</h5>
        <img src="http://placehold.it/500x350"/>
        <p>Echo park kogi thundercats, vice vinyl sustainable 3 wolf moon plaid cornhole marfa 90's helvetica migas humblebrag. Next          level wolf +1 umami.</p>
    </div>
```

Here we are creating a div which holds an image and paragraph inside it.  

You can use an image on your computer, from the internet or a [placeholder](https://placehold.it/).  

Make two more divs, both with the same "each-event" class and place an image and a short paragraph inside each of them.  

Thats enough in our body for now so lets go ahead and finish out our layout with the footer.  

Our footer is going to contain the same navigation links as our header and some social media links.  

First, put the same information in the <nav></nav> links in the header into the footer section.  

Now we'll add social media icons from [Font Awesome](https://fortawesome.github.io/Font-Awesome/). There are over 600 free icons which act just like fonts so you can change their color or size using the same css you would use to change text.  

In the getting started section of the site follow the steps in the *EASIEST: BootstrapCDN by MaxCDN* section. ??? Make sure to place the link *above* your other stylesheets ???? <<check this>>

Now lets add the twitter icon and link it to Twitter. Add the code below right under your "Contact" link.  

```html
    <li><a href="https://twitter.com"><i class="fa fa-twitter"></i></a></li>
```

Notice that because the icon is what we want to display for the link, it is nested *inside* of the anchor tag.  

Add two more icons linking to Facebook and Instagram.  

*********************************************************************************** 
###CSS


From the link [here](https://necolas.github.io/normalize.css/) download the normalize file and copy its contents into the normalize.css stylesheet we created earlier.  

Open the `mystyle.css` document and lets get started.  

First, its important to be organized so we want to create sections that correspond with each section of our html that we'll be styling.  

We have the following sections:
* header
* title div
* main article section
* events section
* footer

These are enough to start with. You can add more sections later if you wish. Its important to start with some type of organizational structure in the beginning and you can always modify this later as you develop your own sense of organization.  

Place the following code in `mystyle.css`.  

```html
/*----------------------------------------*/
/*-----------------HEADER-----------------*/
/*----------------------------------------*/

/*----------------------------------------*/
/*---------------TITLE DIV----------------*/
/*----------------------------------------*/

/*----------------------------------------*/
/*--------MAIN ARTICLE SECTION-----------*/
/*----------------------------------------*/

/*----------------------------------------*/
/*-------------EVENTS SECTION-------------*/
/*----------------------------------------*/

/*----------------------------------------*/
/*-----------------FOOTER-----------------*/
/*----------------------------------------*/
```
These comments will help you stay organized as you begin to manipulate different elements on the page.  

With that done there are couple of other things we should do at the beginning of any project. These are some default values that are often a good idea but not mandatory. As you continue to create projects you'll develop a feel for what things you'll typically want to use.  

Place the code below at the top of your stylesheet above the comments.  

```css  
html {
  box-sizing: border-box;
}

li {
  list-style-type: none;
}

a {
  text-decoration: none;
}
```
 
 The `html` selector sets all items in your html to default to border-box sizing. This means that content, margin and padding are all included inside an elements width automatically.  See lecture notes and/or [W3CSchools](http://www.w3schools.com/css/css3_box-sizing.asp) for more information.  
 
The `li` selectore sets all of your list items to *not* have bullet points. Typically when designing you rarely use lists as actual bullet point lists so this sets the default behavior to exist without the bullets. This is set at the top so you can override it later on in the page if you find yourself needing a "typical" list.  

The `a` selector sets all links ot not be underlined. (Soooooo 90's!)  

Now that we have those basics out of the way...  

Let's start by styling the header.  

```css
nav {
  background-color: teal;
}

a {
  color:white;
}

a:hover {
  color:lightgrey;
}

ul {
  margin:0;
  padding:0;
  display: flex;

}
```
Many elements like `ul`'s have default settings for margin and padding. Here we are setting those to 0 as a base that we can then work from to create our own settings.  

Setting the display to flex makes the ul a container. Its items will default to being set at flex-direction:row (or horizontal). In this case we want our links to be displayed horizontally so that works great and we don't have to do anything more.  

Lets set some space between our list elements so that the css file now looks like this:  
```css
nav {
  background-color: teal;
}

a {
  color:white;
  font-size: 2em;
}

ul {
  margin:0;
  padding:0;
  display: flex;
}

li {
  padding: 15px;
}
```

The title of the page "December" should be centered.  
```css
.month_title {
  display:flex;
  justify-content: center;
}
```


The main article is right up against the edge of the page so adding padding will format that properly.  

```css
.main-article {
  padding: 20px;
}
```

In the events section we want the text to fit neatly below the images they are referencing and the images should fill the whole width of the screen.  

To do this we'll set `each-event` to be a container and set the elements inside it to be stacked in a column instead of the default row direction.  

```css
.each_event {
  display: flex;
  flex-direction: column;
  padding: 20px;
}
```

Finally we can stretch the images to take up the entire width of the screen.

```css

.img {
  width:100%;
}
```

