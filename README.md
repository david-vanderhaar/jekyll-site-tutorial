# ARCHIVED (to keep a log of my development journey)


# Lesson Flow

## Overview of Files and File Structure

1. Define and create most basic files and file structure
* _config.yaml
* _layouts
* _includes
* index.md

### _config.yaml
>This file is where we will define global variables to be used as html throughout our Jekyll site.
>We will access these variables later when we create our first layout
>Let's go ahead and create a title for our website and an owner for our blog
>Inside of our _config.yaml let's type:

	title: My Jekyll Site
	owner: David Vanderhaar

### _layouts
>The files we create inside of our _layouts directory will serve as templates for different pages of out site.
>This is where all of our normal html will live.
>Let's create our first layout and call it default.
>Inside of our _layouts directory, we'll create a file default.html. Now let's put our html boilerplate here.

	<!DOCTYPE html>
	<html lang="en">
		<head>
			<meta charset="UTF-8">
			<title>Title</title>
		</head>
		<body>
			<h1>Hello me!</h1>
		</body>
	</html>

>Now, inside of our body tags type "Hello me!"
>Ok, take a break from layouts. Let's make our first page.

### index.md
>We will write most of our content in markdown so let's create an index.md file in the root of our project.
>This is where the magic starts to happen. Soon we will tell Jekyll to these markdown files and convert them to html.
>Inside of our index.md we want to use our default layout. We will set that up with Yaml front matter. 
>Here's what it looks like:
	---
	layout: default
	---
>What we should see after building our site is the html we typed inside of our default.html
>Let's go to our terminal and get jekyll to build our site. In the root of your project type:
	$ jekyll build
>We should now see a new directory, created by Jekyll, named _site.
>Let's take a look in our browser by typing another command into the terminal
	$ jekyll serve
>Copy the localhost server address that prints out and view in your browser. This is what we shouls see:

![Jekyll Example 1](/img/hello-me.png) 
