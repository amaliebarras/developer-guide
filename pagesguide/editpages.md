---
layout: page
sort: 1
nav_title: Contributing to Pages
---

## Pages Contributor's Guide

This our workflow for editing pages. If you need to create initial setup, please checkout the [COA Pages Setup Guide](../pagessetup.md). If you care to know more about GitHub itself, or standards for using Jekyll or gh-pages directly, checkout the [COA GitHub Guide](../githubguide.md).

### Editing Pages

#### With Prose.io

[Prose.io](http://prose.io) is a tool for editing content on GitHub, with an editing toolbar to help you turn your content into markdown. It's very similar to the editing tools on other blog platforms like Wordpress. [This Prose.io guide](http://www.websbytodd.com/documentation/using-prose/#make-featured-image-available-to-facebook) is written for people who do not know how to code, and is intended for those who are new to using Prose. Check it out for a start to finish guide on editing content with Prose, including screenshots.

#### On GitHub.com

If you want to skip the third party app and just edit on GitHub, there is a way for you to do that, you'll just have to learn some quick markdown. There is more than one workflow for this too, so if you have contributions please share them.

Locate your Pages site's [repository](https://github.com/cityofaustin/pages/tree/master/projects) in the [/projects](https://github.com/cityofaustin/pages/tree/master/projects) directory of the [City of Austin Pages](tps://github.com/cityofaustin/pages) repo.

There should be a list of submodule links like

`projectname @ xxxxxx`

Follow the one that corresponds to your project, then switch to the master branch once you get to your repo.

![](/images/locatemaster.png)

Click into the file that you want to edit. On the top right corner of the file page, click on the pencil icon to edit.

![edit](/images/pencil.png)

Once you make your edits to the content, you will see these fields.

![edit](/images/edit.png)

Unless you are the project owner, you should create a new branch with these edits. It will take you to a flow to create a pull request, which you should follow. The project owner will then get a notification and be able to merge these into the master branch, which in our case corresponds with the live site.

#### Text Editors, Command Line & Git

If you're already familiar with cloning repositories and contributing via a Git workflow, you can always do that too. Whether it's through the command line or using a GUI tool, these work just as well as the editing tools. They just maybe a little overly complicated to learn for this purpose, if that isn't the flow you already work in.

### Learn Markdown

No matter which workflow you use, your end product will be content in a syntax called markdown, which is a file format that gh-pages will turn compile and turn into html. If you are just editing, it's a very quick learning curve.

There is a fantastic [markdown cheatsheet](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf) that GitHub published. The best way to learn is by doing. In the text editor [Atom](https://atom.io/), there is a package called MarkdownPreview which lets you view your markdown as you're writing it. (I'm using it right now!)

![](/images/markdown.png)

##### Basic Syntax

```

# This is an h1

## This is an h2

##### This is an h5

_this is italic_

** this is bold **

* Lists are great
  * This is a list item
  * Make sure you leave space
```

##### Links

```

[link text](http://linkURL.com)
```

##### Adding Images

```

![optional alt text](http://imageurl.com/cat.png)
```

A weird thing about gh-pages, sometimes the images turn sideways on their own.

>This is generally caused by the logical (as opposed to "physical" pixel) orientation being stored in EXIF data that browsers don't read. ImageMagick has an -auto-orient option that fixes it, but I think the easier route may be to save a new (physically rotated) copy from an app like Preview or Photos.

You may have to play with your images a bit to get them oriented right. If you have a solution, feel free to add to the discussion [here.](https://github.com/cityofaustin/pages/issues/19)
