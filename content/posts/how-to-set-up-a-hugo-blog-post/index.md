---
title: "How to Set Up a Hugo Blog Post"
date: 2024-09-25T02:01:58+05:30
description: "Learn how to create a new blog post and embed media into it, using Hugo."
tags: [Hugo]
---
This tutorial covers:

## 1. [How to Create a New Blog Post](#1)

## 2. [How to Add Images to the Blog Post](#2)

## 3. [How to Add Other Media to the Blog Post](#3)

<br />

<h1 id="1">How to Create a New Blog Post</h1>

* Step 1: With PowerShell, navigate to the root of your Hugo website folder, then run the following command:

```sh
hugo new content posts/nameofyourpost/index.md
```
<br />

* Step 2: Open the **content/posts/nameofyourpost/index.md** file in your favorite code editor. Go to the front matter, or section in between the "---" triple hyphens, and edit the following:

- For **title:**, type the title of the blog post.
- For **date:**, type the date of the blog post. The Hugo date format is **YYYY-MM-DD**.
- For **description:**, type a preview or teaser of what the post is about. This description will appear in the blog feed (if using the Archie theme).
- For **tags:**, type **[nameoftag]** or **[tag1, tag2]**. Make sure to capitalize and alphabetize these, as Hugo does not do this automatically.

* Step 3: Edit your blog post however you like, using Markdown. 

<h1 id="2">How to Add Images to the Blog Post</h1>

Step 1: Copy and paste the desired image file(s) into your **content/posts/nameofyourpost/** directory.

Step 2: In your index.md file, add the following Markdown:

```
![Alt text](image_path "title text")
```

<br />

For example, if I have an image called "broccoli.png", then I would add it to my blog post with:

```
![A picture of broccoli](broccoli.png "A picture of broccoli")
```

<br />

If you want more control over the CSS styling of the image, please see the next section.

<h1 id="3">How to Add Other Media to the Blog Post</h1>

- Step 1: In order to embed media with \<iframe> tags, we need to specify that Hugo uses the Goldmark flavor of Markdown. First open the hugo.toml file in the root of your Hugo blog directory.

<br />

- Step 2: In the hugo.toml file, go below the **publishDir = "docs"** and above the **[params]** table, and paste this code:

```
[markup]
   [markup.goldmark]
      [markup.goldmark.renderer]
         unsafe = true
```

<br />

* Step 3: Open your **content/posts/nameofyourpost/index.md** file and paste the desired media tags. For example, to paste a Youtube video, add:

```
<iframe class="BLOG_video_class" allowfullscreen="" youtube-src-id="K9PKaFHIHN4" width="100%" height="416" src="https://www.youtube.com/embed/K9PKaFHIHN4"></iframe>
```

<br />

With Goldmark, you can embed html tags. Thus, you can embed your images, video, and other media inside \<div> tags for more fine-grained control over their CSS styling.

<br />

Note: Hugo uses shortcodes to embed images and video, but the CSS of these shortcodes cannot be easily edited.

<br />

Now you know how to create Hugo blog posts. The next tutorial will cover how to edit the CSS of an Archie theme Hugo blog.

<br />



