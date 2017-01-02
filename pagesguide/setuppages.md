---
layout: page
sort: 2
nav_title: Setting Up A Project in Pages
---

## Pages Setup Guide

This our workflow for creating a Pages project. If you simply need to edit a page, checkout the [COA Contributor's Guide](../editpages.md). If you care to know more about GitHub itself, or standards for using Jekyll or gh-pages directly, checkout the [COA GitHub Guide](../githubguide.md).

### Workflow Example
I'm sure there are many other ways to do this, this is just one I've found to work. We welcome your suggestions and contributions on this [wiki.](#)

#### Prerequisites

You'll need a few tools for this workflow.

* Terminal
  * You can use mac's native terminal or download a fancy one like [iTerm](https://www.iterm2.com/)
* Text Editor
  * [Atom](http://atom.io) has a markdown preview package which will come in handy later.
* Github Account
  * Sign up for credentials on [github](https://github.com/). You can do things like: fill out your profile, follow your friends, and get added to the to [City of Austin Organization](https://github.com/cityofaustin/) another time

### Set Up Repository

#### Locate

Locate your Pages site's [repository](https://github.com/cityofaustin/pages/tree/master/projects) in the [/projects](https://github.com/cityofaustin/pages/tree/master/projects) directory of the [City of Austin Pages](tps://github.com/cityofaustin/pages) repo.

If you don't currently see your project listed, you should submit an [issue](https://github.com/cityofaustin/pages/issues) on the pages repo requesting one.

There should be a list of submodule links like

`projectname @ xxxxxx`

follow the one that corresponds to your project, then switch to the master branch once you get to your repo.

![](/images/locatemaster.png)

#### Connect Local Git to Remote

As a prerequisite for this step, you'll need to follow the steps under "Install Git" in [this tutorial](https://www.atlassian.com/git/tutorials/install-git/)

In your repo, copy the link to clone using HTTPS
![](/images/clone.png)

Open your Terminal where you just installed Git, and type `git clone ` followed by the link you just copied.

Make a slight change to your README.md file, and then push a commit.

`git add README.md`

`git commit -m "first commit"`

`git push origin master`

Check the repository to see if your update hit.

Congrats, you're now set up to make commits to your master branch.

#### Create File Structure

For this step, I'd recommend creating an outline for how you want your navigation to look

*******
e.g.

* Intro
* Background
  * Our Team
  * Project Timeline
* Findings
******

Once you have an idea what the structure will be, you can create files. I recommend using your desktop explorer or finder while you create these files. You can create these files from the command line using `touch` if you know how to, or you can open a text editor like [Atom](https://atom.io/
).

Start with the highest level of pages first.

Our intro page is going to be the landing page for our project site, so you'll want to name the file `index.md`
.md stands for markdown, which is a file format that gh-pages will turn compile and turn into html. More on markdown later. The index file tells the browser to show it first, and show other pages relative to it.

Next, for other pages that you never plan to add sub-navigation pages to, you can go ahead and create those in the root of the directory (just inside the directory folder.) In our example, that would be intro (which we just created as index.md) and `findings.md`.

Pages that will have nested pages need to go in a folder. In our example, we can use Background.

![](/images/files.png)

Within background, you'll create an `index.md` for the background landing page within the background section, and two files, `team.md` and `timeline.md` for each of the nested pages.

Once you have your file structure all framed out, you'll have to tell github a little more about the files using Front Matter.

#### Add Front Matter

Every single .md file that you create will need Front Matter at the top. Front Matter looks like this:

```

---
title: Project Name
nav_title: Intro
layout: page
sort: 1
---

```

The `project title` will be the same throughout the whole directory and `layout` is always going to be page unless you know otherwise.

The two things that will change from file to file are `nav_title` and `sort`. Your `nav_title` is easy, it's just going to be the title of the page you're writing. `Sort` is trickier. Let's look at our example again

*******

* Intro
* Background
  * Our Team
  * Project Timeline
* Findings
******

You're going to start with the top most level of pages first. So intro or `index.md` would be `sort: 1`, Background, or `background/index.md` would be `sort: 2`, and `findings.md` would be `sort: 3`.

Then, within each section that contains the nested tabs, you'll do the sort relevent to that sections index.md

so `background/index.md` would be `sort: 2`, but `background/team.md` would also be `sort: 2` since it's the second page in the directory. then `timeline.md` would be `sort: 3`.

*******

* Intro | index.md | Sort: 1
* Background | background/index.md | Sort: 2
  * Our Team | background/team.md | Sort : 2
  * Project Timeline | background/timeline.md | Sort : 3
* Findings | findings.md | Sort: 3
******

### Time to Commit

Once you have your Front Matter and File Structure in order, you can commit to master using the commands from earlier.

`git add .`

The ``.`` means all files

`git commit -m "initial file structure"`

`git push origin master`

Wait a few minutes for gh-pages to compile your files and build your site, and your new structure will appear live on Pages.

Now, you can start filling in content using the [contributor's workflow.](../editpages.md)

### Initial Content Workflow

I would strongly recommend using [Google Docs](http://docs.google.com/) for editing content. It's much easier to spend a few minutes at the end of a week of editing turning a [word document into markdown](http://word-to-markdown.herokuapp.com/) and commit finalized changes at once, than it is to get tangled in pull requests and branches. The disadvantage is that the edits aren't happening out in the open, but if you're diligent about regularly publishing at milestones, this is a fine workaround.
