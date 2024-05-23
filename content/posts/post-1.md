---
title: "Cheese"
date: 2020-04-01T02:01:58+05:30
description: "Microsoft Sticky Notes does more than just note-taking. Insert images, hyperlinks, and even customize the sticky note color. Learn how to open the Sticky Notes app on Windows 11."
tags: []
---

This tutorial covers:
1. <a href="#1">What is the Microsoft Sticky Notes App?</a>
2. <a href="#2">How to Open the Microsoft Sticky Notes App With Search</a>

<br />
<p>No time to scroll down? Click through this tutorial presentation:</p>


Watch a tutorial video here:


<h1 id="1">What is the Microsoft Sticky Notes App?</h1>

Sticky Notes is a note-taking app that comes with Windows 11. Notes can have formatted text (bold, italic, underline, strikethrough, and bulleted lists), images, and recognized URLs. For further customization, choose from seven different colors of sticky notes and a "Dark" mode for the app.


<h1 id="2">How to Open the Sticky Notes App With Search</h1>

*Step 1: Go down to the taskbar and click Start (four blue squares). <div class="stepimage">![A screenshot of the cursor clicking the Start (four blue squares) button on the lower left side of the taskbar at the bottom of the screen.](../../static/watermark.png "Click the Start button")</div>

*Step 2: In the Start window that opens, click the top search bar and type "sticky notes". <div class="stepimage">![A screenshot of the cursor clicking the search bar at the top of the Start window.](blogstartbuttonedit.png)</div>

*Step 3: On the search results screen, click one of the following to open the Sticky Notes app. <div class="stepimage">![A screenshot of the search results, with three blue rectangles surrounding the "Sticky Notes App" and "Open" buttons.](post1/watermark.png)</div>

Troubleshooting the image paths
If the current post file is in content/posts, then the path should go back from posts to content, go back from content to root, from root to static, then images, then the image ../../static/images/blogstartbuttonedit.png
Should not be this, because posts goes back to content which is in the root

![A screenshot of the cursor clicking the Start (four blue squares) button on the lower left side of the taskbar at the bottom of the screen.](c:\Users\jamiy\github\qhtutorials.github.io\static\watermark.png "Click the Start button")

Cheese

<div class="stepimage">![Is this really an image?](blogstartbuttonedit.png)</div>


cheese

<img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjhyphenhyphenyKz6H6GBf0L6rAA9Yv6HHBWpU2eNr9LA7x5eV5EJzwBQOkMhnSi0DyAUQmk7UjlTQmcpWCL-Q7VxslYxEP56LQyvDwpBRQhiBTPJYMashGedPdoFqOgR3XmqDq947xpOnFNKhio5gDqpe7hbKQPRLpKXDgliuxJFk_mI24T7LndC8zu3lwzXFjr4TQ/s800/blogstartbuttonedit.png" alt text="A screenshot of the cursor clicking the Start (four blue squares) button on the taskbar at the bottom of screen." title="Click the Start button" height="250px">


Even when I click the goddamn vscode link, it still doesn't work. It knows that it's an image, but it just won't link to it. Otherwise the alt text wouldn't appear

{{< figure src="../" title="A screenshot of the cursor clicking the Start (four blue squares) button on the lower left side of the taskbar at the bottom of the screen." >}}


Or ../../assets/images/blogstartbuttonedit.png. Can't be this

Or blogstartbutonedit.png. This doesn't work

Or ../blogstartbuttonedit.png this shouldn't work because you didn't specify the static folder

Or ../static/blogstartbuttonedit.png 

Or ../static/images/blogstartbuttonedit.png

Or perhaps the file is not the post file, but the html file which is single.html, so layouts/_default/single.html, so ../to go to layouts, ../ to go to root, then static/images/filename
../../static/images/filename. But this doesn't work


Future posts will cover more features of the Sticky Notes app, so stay tuned!

<br />