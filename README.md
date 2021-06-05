## Project Summary

In this project, we will learn how to use css media queries to help us make our websites be responsive to different screen sizes. We can make out website look a different way on mobile, tablet and desktop devices. We are going to practice what is called "mobile first development". Our styles will start with what we want the website to look like on a mobile device, and then we will add media queries to adjust the styles for tablets and desktops.

Using our chrome developer tools is a great way to help us simulate being on different devices. Click `cmd opt j` to open the developer tools pane, and you can click on the devices icon on the top left side of the pane.

[insert picture]

You can then pick a device you want to simulate.

[insert picture]

Pretty cool, right?! Let's start writing code :)

## Steps

After each step, use git to add and commit the changes you have made to the project!

### Step 1.

Fork this repository to create your own copy.

### Step 2.

Make `index.html` and `style.css` files. Use HTML:5 snippet and link the style sheet to the html. We will also want to link the `reset.css` file that is included in the repo. Make sure to link `reset.css` before `style.css` so that the reset styled are applied first.

In this step, let's also go ahead and change the title for our website. You can make it whatever you want.

In our `style.css` file, let's add some media queries for each of the different device types we want to handle. We won't do anything with these right now, but let's go ahead and add them so we can use them later. It's is totally noraml to be confused at this point. So don't feel overwhelmed just yet :)

<details>
<summary>index.html</summary>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="reset.css" />
    <link rel="stylesheet" href="style.css" />
    <title>Media Queries</title>
  </head>
</html>
```

</details>

<details>
<summary>style.css</summary>

```css
/* tablet */
@media screen and (min-width: 481px) {
}

/* small screens, laptops */
@media screen and (min-width: 769px) {
}

/* desktops, large screens */
@media screen and (min-width: 1025px) {
}

/* extra large screens, TV */
@media screen and (min-width: 1201px) {
}
```

</details>

### Step 3.

Let's create a header first. Remember we want to start with what we want the header to look like on mobile first. Here's a picture of what we are wanting to create.

[insert picture here]

Since there is nothing else on our website right now, let's go ahead and give the header a border-bottom that we will remove later.

<details>
<summary>index.html</summary>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="reset.css" />
    <link rel="stylesheet" href="style.css" />
    <title>Media Animations</title>
  </head>
  <body>
    <header>
      <h1>Thailand</h1>
      <div id="mobile-ham-menu"></div>
    </header>
  </body>
</html>
```

</details>

<details>
<summary>style.css</summary>

```css
header {
  position: fixed;
  width: 100%;
  background: white;
  padding: 16px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 80px;
  border-bottom: 1px solid black;
}

#mobile-ham-menu::after {
  content: "\2630";
  font-size: 24px;
}

/* tablet */
@media screen and (min-width: 481px) {
}

/* small screens, laptops */
@media screen and (min-width: 769px) {
}

/* desktops, large screens */
@media screen and (min-width: 1025px) {
}

/* extra large screens, TV */
@media screen and (min-width: 1201px) {
}
```

</details>

### Step 4.

Now let's make our header have navigation links instead of a hamburger menu if the website is being viewed on a desktop.

[insert image here]

<details>
<summary>index.html</summary>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="reset.css" />
    <link rel="stylesheet" href="style.css" />
    <title>Media Animations</title>
  </head>
  <body>
    <header>
      <h1>Thailand</h1>
      <div id="mobile-ham-menu"></div>
      <nav>
        <a href="#store">Store</a>
        <a href="#blog">Blog</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>
  </body>
</html>
```

</details>

<details>
<summary>style.css</summary>

```css
header {
  position: fixed;
  width: 100%;
  background: white;
  padding: 16px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 80px;
  border-bottom: 1px solid black;
}

#mobile-ham-menu::after {
  content: "\2630";
  font-size: 24px;
}

nav {
  display: none;
}

/* tablet */
@media screen and (min-width: 481px) {
}

/* small screens, laptops */
@media screen and (min-width: 769px) {
  #mobile-ham-menu {
    display: none;
  }

  nav {
    display: block;
  }
}

/* desktops, large screens */
@media screen and (min-width: 1025px) {
}

/* extra large screens, TV */
@media screen and (min-width: 1201px) {
}
```

</details>

### Step 5.

Let's create an image banner for our website. On mobile we will want the banner to fill the screen and we will have some text in it.

[insert image here]

<details>
<summary>index.html</summary>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="reset.css" />
    <link rel="stylesheet" href="style.css" />
    <title>Media Animations</title>
  </head>
  <body>
    <header>
      <h1>Thailand</h1>
      <div id="mobile-ham-menu"></div>
      <nav>
        <a href="#store">Store</a>
        <a href="#blog">Blog</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>
    <div id="content-wrapper">
      <div class="banner">
        <h1>Welcome</h1>
        <h1>to</h1>
        <h1>Thailand</h1>
      </div>
    </div>
  </body>
</html>
```

</details>

<details>
<summary>style.css</summary>

```css
header {
  position: fixed;
  width: 100%;
  background: white;
  padding: 16px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 80px;
  border-bottom: 1px solid black;
}

#mobile-ham-menu::after {
  content: "\2630";
  font-size: 24px;
}

nav {
  display: none;
}

#content-wrapper {
  padding-top: 80px;
}

.banner {
  background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)),
    url("https://images.unsplash.com/photo-1520250497591-112f2f40a3f4?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=2250&q=80");
  width: 100%;
  height: calc(100vh - 80px);
  background-position: center;
  background-size: cover;
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.banner h1 {
  font-size: 48px;
  line-height: 72px;
}

/* tablet */
@media screen and (min-width: 481px) {
}

/* small screens, laptops */
@media screen and (min-width: 769px) {
  #mobile-ham-menu {
    display: none;
  }

  nav {
    display: block;
  }
}

/* desktops, large screens */
@media screen and (min-width: 1025px) {
}

/* extra large screens, TV */
@media screen and (min-width: 1201px) {
}
```

</details>

### Step 6.

Let's make this banner section responsive for other devices.

[insert image here]

<details>
<summary>index.html</summary>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="reset.css" />
    <link rel="stylesheet" href="style.css" />
    <title>Media Animations</title>
  </head>
  <body>
    <header>
      <h1>Thailand</h1>
      <div id="mobile-ham-menu"></div>
      <nav>
        <a href="#store">Store</a>
        <a href="#blog">Blog</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>
    <div id="content-wrapper">
      <div class="banner">
        <h1>Welcome</h1>
        <h1>to</h1>
        <h1>Thailand</h1>
      </div>
    </div>
  </body>
</html>
```

</details>

<details>
<summary>style.css</summary>

```css
header {
  position: fixed;
  width: 100%;
  background: white;
  padding: 16px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 80px;
  border-bottom: 1px solid black;
}

#mobile-ham-menu::after {
  content: "\2630";
  font-size: 24px;
}

nav {
  display: none;
}

#content-wrapper {
  padding-top: 80px;
}

.banner {
  background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)),
    url("https://images.unsplash.com/photo-1520250497591-112f2f40a3f4?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=2250&q=80");
  width: 100%;
  height: calc(100vh - 80px);
  background-position: center;
  background-size: cover;
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.banner h1 {
  font-size: 48px;
  line-height: 72px;
}

/* tablet */
@media screen and (min-width: 481px) {
}

/* small screens, laptops */
@media screen and (min-width: 769px) {
  #mobile-ham-menu {
    display: none;
  }

  nav {
    display: block;
  }

  .banner {
    flex-direction: row;
  }

  .banner h1 {
    margin: 0 12px;
  }
}

/* desktops, large screens */
@media screen and (min-width: 1025px) {
  .banner h1 {
    font-size: 72px;
  }
}

/* extra large screens, TV */
@media screen and (min-width: 1201px) {
}
```

</details>

### Step 7.

Do what you want in this step! Just practice using media queries and have fun with it. If you are following along with the video (which I hope you are), I will create a small section under the banner image, but you can do what you want!

[insert image here]

<details>
<summary>index.html</summary>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="reset.css" />
    <link rel="stylesheet" href="style.css" />
    <title>Media Animations</title>
  </head>
  <body>
    <header>
      <h1>Thailand</h1>
      <div id="mobile-ham-menu"></div>
      <nav>
        <a href="#store">Store</a>
        <a href="#blog">Blog</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>
    <div id="content-wrapper">
      <div class="banner">
        <h1>Welcome</h1>
        <h1>to</h1>
        <h1>Thailand</h1>
      </div>
      <section>
        <h1>My Favorite Place</h1>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum ea esse
        nulla, exercitationem voluptatem, nobis perspiciatis obcaecati
        voluptates nihil molestias corporis dolor ipsa aspernatur expedita
        cupiditate delectus! Amet, ad facere.
      </section>
    </div>
  </body>
</html>
```

</details>

<details>
<summary>style.css</summary>

```css
header {
  position: fixed;
  width: 100%;
  background: white;
  padding: 16px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 80px;
  border-bottom: 1px solid black;
}

#mobile-ham-menu::after {
  content: "\2630";
  font-size: 24px;
}

nav {
  display: none;
}

#content-wrapper {
  padding-top: 80px;
}

.banner {
  background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)),
    url("https://images.unsplash.com/photo-1520250497591-112f2f40a3f4?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=2250&q=80");
  width: 100%;
  height: calc(100vh - 80px);
  background-position: center;
  background-size: cover;
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.banner h1 {
  font-size: 48px;
  line-height: 72px;
}

section {
  padding: 24px 16px;
}

section h1 {
  font-size: 28px;
  margin-bottom: 24px;
}

/* tablet */
@media screen and (min-width: 481px) {
}

/* small screens, laptops */
@media screen and (min-width: 769px) {
  #mobile-ham-menu {
    display: none;
  }

  nav {
    display: block;
  }

  .banner {
    flex-direction: row;
  }

  .banner h1 {
    margin: 0 12px;
  }

  section {
    padding: 48px 32px;
  }

  section h1 {
    font-size: 32px;
    margin-bottom: 24px;
  }
}

/* desktops, large screens */
@media screen and (min-width: 1025px) {
  .banner h1 {
    font-size: 72px;
  }
}

/* extra large screens, TV */
@media screen and (min-width: 1201px) {
}
```

</details>

## Submit project

The final step, and one of the most important! Use git to add and commit any new changes, then push those changes to your reposiroty on github.

You did it! You created a responsive website! Congratulations! Make sure you submit this project in the `Guided project(s)` section for this unit. Just copy the url for your repository, paste it and click send!

## Solution

<details>

<summary>index.html</summary>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="reset.css" />
    <link rel="stylesheet" href="style.css" />
    <title>Media Animations</title>
  </head>
  <body>
    <header>
      <h1>Thailand</h1>
      <div id="mobile-ham-menu"></div>
      <nav>
        <a href="#store">Store</a>
        <a href="#blog">Blog</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>
    <div id="content-wrapper">
      <div class="banner">
        <h1>Welcome</h1>
        <h1>to</h1>
        <h1>Thailand</h1>
      </div>
      <section>
        <h1>My Favorite Place</h1>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum ea esse
        nulla, exercitationem voluptatem, nobis perspiciatis obcaecati
        voluptates nihil molestias corporis dolor ipsa aspernatur expedita
        cupiditate delectus! Amet, ad facere.
      </section>
    </div>
  </body>
</html>
```

</details>

<details>

<summary>index.css</summary>

```css
body {
  display: flex;
  flex-direction: column;
  height: 100vh;
}

header {
  background: white;
  padding: 16px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 80px;
}

#mobile-ham-menu::after {
  content: "\2630";
  font-size: 24px;
}

#content-wrapper {
  flex: 1;
  overflow: auto;
}

.banner {
  background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)),
    url("https://images.unsplash.com/photo-1520250497591-112f2f40a3f4?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=2250&q=80");
  width: 100%;
  height: 100%;
  background-position: center;
  background-size: cover;
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.banner h1 {
  font-size: 48px;
  line-height: 72px;
}

nav {
  display: none;
}

section {
  padding: 24px 16px;
}

section h1 {
  font-size: 28px;
  margin-bottom: 24px;
}

/* tablet */
@media screen and (min-width: 481px) {
  .banner {
    height: 500px;
  }
}

/* small screens, laptops */
@media screen and (min-width: 769px) {
  #mobile-ham-menu {
    display: none;
  }

  nav {
    display: block;
  }

  .banner {
    flex-direction: row;
  }

  .banner h1 {
    margin: 0 12px;
  }

  section {
    padding: 48px 32px;
  }

  section h1 {
    font-size: 32px;
    margin-bottom: 24px;
  }
}

/* desktops, large screens */
@media screen and (min-width: 1025px) {
  .banner h1 {
    font-size: 72px;
  }
}

/* extra large screens, TV */
@media screen and (min-width: 1201px) {
}
```

</details>
