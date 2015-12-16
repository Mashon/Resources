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
  
  
