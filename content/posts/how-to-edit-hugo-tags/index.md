---
title: "How to Edit Tags in a Hugo Blog"
date: 2024-10-21-T02:01:58+05:30
description: "Learn how to add and edit Hugo blog tags."
tags: [Hugo]
---
This tutorial covers:

## 1. [How to Add Tags to a Hugo Blog Post](#1)

## 2. [How to Edit the Tags Page in the Archie Theme](#2)

## 3. [How to Edit Tags on a Blog Page](#3)

<br />

<h1 id="1">How to Add Tags to a Hugo Blog Post</h1>

* Step 1: Open one of your Hugo blog post index.md files, and in the front matter insert the following:

```
tags: [tag1, tag2]
```
Make sure to capitalize and alphabetize the tags, as Hugo does not do this automatically.

<br />

<h1 id="2">How to Edit the Tags Page in the Archie Theme</h1>

* Step 1: In the root directory of your Hugo blog, navigate to the layouts/_default/term.html and edit this file however you like. For example, you can change the `All Entries Tagged:` to `Entries Tagged:`.

Or you can add another section to the Tags page, by inserting your desired code before the closing `{{end}}` tag, like so:

```
All Articles

{{end}}
    {{-range.Data.Pages-}}{{- if (not(in (.Site.Params.excludedTypes | default (slice "page")) .Type)) -}}
    {{.Title}} {{dateFormat "Jan 2, 2006" .Date}}{{ if .Draft}} DRAFT {{end}}
    {{-end -}}{{- end -}}

Place your content here

{{end}}

```
You can add a section such as "All Tags", or a link back to the main blog page. The sky is the limit!

<br />

<h1 id="3">How to Edit Tags on a Blog Page</h1>

- Step 1: Open the layouts/_default/single.html file and edit this section however you like:

```html
<div class="post-tags">
			{{ if ne .Type "page" }}
			{{ if gt .Params.tags 0 }}
			<nav class="nav tags">
				<ul class="tags">
					{{ range .Params.tags }}
					<li><a href="{{ "/tags/" | relLangURL }}{{ . | urlize }}">{{ . }}</a></li>
					{{ end }}
				</ul>
			</nav>
			{{ end }}
			{{ end }}
		</div>
```

For example, you can wrap this code in another `<div>` with a custom class, and then customize the CSS of the tags with that class. 

<br />




