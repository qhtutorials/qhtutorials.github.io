---
title: "How to Edit CSS in the Archie Theme"
date: 2024-10-04T02:01:58+05:30
description: "Want to make the Archie Hugo theme your own? This tutorial explains how to edit the CSS of your blog."
tags: [Hugo, CSS]
---
This tutorial covers:

## 1. [How to Add Custom CSS to the Archie Theme](#1)

## 2. [How to Edit the CSS of the Archie Theme](#2)

## 3. [How to Change the Font of the Archie Theme](#3)

<br />

<h1 id="1">How to Add Custom CSS to the Archie Theme</h1>

* Step 1: In the root directory of your Hugo blog, open the hugo.toml file, and add this line:

```
[params]
   customcss = ["css/first.css"]
```
<br />

* Step 2: Use Visual Studio Code or your favorite editor to create the assets/css/first.css file. Copy and paste all the contents from the Archie theme main.css into your first.css file.  

<br />

* Step 3: Edit the CSS in the first.css file any way you like. The following section gives some examples of how to customize the CSS. 

<h1 id="2">How to Edit the CSS of the Archie Theme</h1>

##### To change the color of the hyperlinks: 

* Under the ```root:{}``` selector delete the ```--maincolor: red;``` property. 
* Locate the ```a{}``` property and change ```color: #000000;``` to the desired color.

##### To remove the underline of the hyperlinks:

*  In the ```a:hover {}``` selector, change the ```border-bottom: ``` property to ```border-bottom: none;``` to remove this. 
* Otherwise, specify the desired properties, such as ```border-bottom: 2px solid #000000;```. 

##### To edit the h1 through h6 headers:

* Find the ```h1::before {}``` to ```h6::before {}``` selectors, and change the ```content: '# '; ``` property to ```content: none;``` to remove the # symbols before the headers.
* To specify different sizes for each header, remove the

```css
h1, h2, h3, h4, h5, h6 {
  font-size: 1.2rem;
  margin-top: 2em;
}
```

and replace it with

```css
h1 {font-size: 2rem; line-height: 40px;}
    h2 {font-size: 1.7rem;}
    h3 {font-size: 1.5rem;}
    h4 {font-size: 1.2rem;}
    h5 {font-size: 1rem;}
    h6 {font-size: 0.8rem;}
```

You can adjust the size values as needed.

##### To change the horizontal rule at the bottom:

* Locate the ```root:{}``` selector and change the ```--bordercl: rebeccapurple;``` to ```--bordercl: #737373;```, or another desired color.
* Under the ```hr {}``` selector, replace

```css
hr {
  border: 0;
  border-top: 3px dotted var(--bordercl);
  margin: 1em 0;
}
```

with 

```css
hr {
       border-top: 1.5 px solid #737373;
    }
```

Now the line of purple dots should be replaced with a grey line. 

<br />

<h1 id="3">How to Change the Font of the Archie Theme</h1>

- Step 1: First go to a font website, such as [fontsquirrel.com](https://www.fontsquirrel.com/), and download a font (it can be a .otf, .eot, .ttf, .woff, .woff2, or svg file).

<br />

- Step 2: In the first.css file, add the font to the CSS. For example, to add the Merriweather font, paste this near the font section:

```css
    /* Merriweather-Regular */
@font-face {
    font-display: swap;
    font-family: 'Merriweather-Regular';
    font-style: normal;
    font-weight: 400;
    src: url('../fonts/Merriweather-Regular.otf')
}
```

- Step 3: Now apply the font to specific html elements. 
    - Go to the corresponding selector and add the property of ```font-family: 'Merriweather-Regular'; ```. 
    - For example, to make ordered lists have the Merriweather font, edit the first.css file with:

```css
ol {
        font-family: 'Merriweather-Regular';
    }
```

<br />

You are one step closer to making your blog unique! In the next post, learn how to edit the Hugo blog tags.

<br />



