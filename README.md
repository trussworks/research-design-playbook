# Welcome to the Truss Research and Design Playbook

## Purpose of this Playbook:

Within Truss we have a wealth of opinions and experiences regarding design, research, and content strategy best practices, tools, approaches, and practices. The problems and choices that we encounter in our day-to-day practice are rarely new. Having a straightforward way of applying the things we collectively know to the problems we face would be a source of great efficiency for us and also a boon to the design and research communities.

This collection of resources is intended to be simple and searchable, each one containing the essence of Truss opinions. Whilst any Trussel is free to edit these documents, there is some expectation that these are to be ultimately owned and curated by the members of the design practice at Truss. To that end, proposed changes should be submitted via a pull request and leads will be identified to act as curators for particular knowledge areas.

## Playbook How-To:

This playbook uses a static site generator called [Jekyll](https://jekyllrb.com/). Jekyll allows easy editing of content files using markdown. If you're not familiar with markdown syntax, check out the handy dandy guide labeled `markdowncheatsheet.md` in the main directory folder.

We are also using a Jekyll template/theme called [Just the docs](https://pmarsceill.github.io/just-the-docs/). You shouldn't need to make any edits to the template/theme when contributing content to the playbook, however if you need to or are interested please review the theme [documentation](https://pmarsceill.github.io/just-the-docs/).

### Ways to contribute to the playbook

There are a couple of ways you can contribute to the playbook:
1. **For those who would like to use Github to edit content:** Login and use the GitHub interface to make edits and pull requests
2. **For those familiar with editing a repository locally:** Clone the repository to your computer and work locally using a text editor to make the edits you desire and terminal or github desktop to pull and then push any new changes

### How to make edits

- A majority of the content files are located in the `docs` directory
- Inside the `docs` directory you will find each page as separate markdown file
- Editing/removing/adding markdown files to this directory will update the content in the playbook

**What is this section at the top of each markdown file?**

```
---
layout: default
title: Copy Style Guide
nav_order: 5
---
```

This block is called **front matter** it tells the site what page layout to use, what the title of the page shoud be, and where to include the page in the navigation.

- **layout:** you shouldn't need to change this property, we will use the `default` layout for all playbook pages for now
- **title:** this is the title of the page that will show in the browser's title bar or page's tab
- **nav_order:** this is the placement of the page in the side bar navigation

For more details on the front matter refer to these [docs](https://pmarsceill.github.io/just-the-docs/docs/navigation-structure/#pages-with-children)

### Creating pull requests for changes

After you have made edits please open up a new pull request for someone else to review your edits before pushing changes to the site.

### How to use github to create commits and start pull requests
- After making changes to a file you'll see a section to commit your changes
- Add a title to your commit with a brief description of the change that you made
- Select the option "Create new branch for this commit and start a pull request"
- Title your new branch with with the following format: `[your initials] - [brief description of the change]` (e.g. jf-navigation-update)
![](https://github.com/trussworks/research-design-playbook/blob/master/contribution-guidelines/github-commit-with-details.png)
- After you **propose file change** you will be taken to a page to start a new pull request

### Writing your pull requests

Please use the following format for creating your pull request.

**Title**
`[your initials] - [breif description of changes made]`

**Body**
```
Page(s) edited: [list of page(s) edited]
Edits made: [description or list of edits made]
Additional notes (optional): [any additional notes you may want reviewers to know about]
```

After you have created your pull request please add **reviewers** to the PR (PR reviewers TBD). This will notify someone to take a look and approve your changes.

## Setting up the site on your local machine:

- Clone the repo onto your machine:
```
git clone git@github.com:trussworks/research-design-playbook.git
```

- Navigate into the project:
 ```
 cd research-design-playbook
 ```

Then choose one of the two methods below to run the site, which will be available
at [http://localhost:4000/](http://localhost:4000/).

### Docker

If you have Docker installed you can run the following without managing Ruby on your system:

```sh
docker run -it --rm=true -v $PWD:$PWD -w $PWD -p 4000:4000 ruby:2.7.2 /bin/bash -c "gem install bundler:2.2.16 && bundle install && bundle exec jekyll serve --host 0.0.0.0"
```

### Local Ruby

If you don't already have a proper Ruby environment, use
[Moncef's script](https://github.com/monfresh/install-ruby-on-macos#install) for
the easiest way to get set up.

If you already have a working Ruby environment, make sure it's up to date:
```shell
gem update --system
gem update bundler
```

You might also need to install Ruby 2.7.2 if you don't already have it. If you
used Moncef's script, you already have it. If you didn't use Moncef's script,
and you don't know how to install specific versions of Ruby, reach out to
Moncef and he will sort you out in no time.

Once Ruby is in order, you can install the dependencies and start the Jekyll
server:

```shell
bundle install
bundle exec jekyll serve
```

Woohoo! Great job! If you run into any trouble or have questions, please reach out to Moncef (Ruby expert) or Josh (design).
