---
layout: page
sort: 3
nav_title: GitHub 101 & Added Context
---

## Pages Github Guide

This page contains information and standards about how the City of Austin uses GitHub. If you need to set up a pages project, check out the [COA Pages Setup Guide](../pagessetup.md). Or, if you simply need to edit a page, checkout the [COA Contributor's Guide](../editpages.md).

### Basic GitHub Guidance

There is an excellent github tutorial for beginners [here](https://guides.github.com/activities/hello-world/). The following guide will supplement this guide with City of Austin-specific information.

#### Repositories

To manage a project on Pages, there are two repositories you need to care about.

* First is the overall [Pages](https://github.com/cityofaustin/pages) repository. This one contains all the styles, configuration, and come context and developer information for City of Austin Pages.

* Second is your individual project repository, where all your content will live. You can get to those from the [project directory](https://github.com/cityofaustin/pages/tree/master/projects) of Pages. These are connected to the Pages site through something called a [submodule]().

For [pages.austintexas.io](http://pages.austintexas.io/) you'll commit content changes to the project repo, not the Pages repo.

#### Branches

The master branch is by default the main branch that will appear when someone visits your repo on GitHub.com, and is also the branch that communicates with gh-pages to build your live project page. When you change the master branch, the site rebuilds. It is a good practice to work out of a non-master branch to make multiple changes, and then create a pull request to merge those changes into the master. That way, you can save often, but your site isn't rebuilding every 10 minutes.

#### Commits

In order to save changes, you have to commit them. If you're working out of a branch called 'edits', you'll push your commits to the 'edits' branch. When you're done with making changes for a while and you're ready to see them live on your project site, you'll create a pull request to merge that branch into master.

#### Pull Requests

Pull requests allow you to let your collaborators know you're making a change, both creating a gatekeeping opportunity for project owners, as well as providing an interface for getting feedback from comments and peers.

##### Creating Pull Requests

In our workflow, you'd use the 'edits' branch as the base, to compare with 'master' which is the one you want to merge into.

##### Merging Pull Requests

If you are the project owner, you can usually merge your own commits, and if you are a collaborator, you'll have to wait for your pull request to be merged by a project owner.

### Issues

A great thing to do if you have a question about something happening on a GitHub repository is to report it via an [Issue](https://guides.github.com/features/issues/).

If you have a question about styling, adding a project, or general setup, it is probably best to post that in the overall pages repo. If you have a comment about a piece of content in a specific project, you should post that issue in the project repo.

### Standards

COMING SOON
