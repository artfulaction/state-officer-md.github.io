The State Officer, M.D. (SOMD) site will need some care and feeding over time. This document captures the likely process that ongoing maintenance and development will entail.

# Editing - Remote or Local?

You can work on this content remotely (or, directly on the site), or you can work locally.

## Working Remotely

It is possible to edit this site directly on Github. 

For example, [you can edit the README](https://github.com/state-officer-md/state-officer-md.github.io/edit/main/README.md). Click on that link; if you are a member of the repository, then you will be presented with an editing interface. Any changes you make (and save) will *immediately* be reflected in the live site. 

When making changes, you should always make sure you leave a meaningful commit message. For minor edits and spelling corrections, you might just say "Correcting typos." For more substantial edits, you should probably leave a brief explanation of what you changed (and why).

**Working remotely is "dangerous" in that all changes immediately go live. Remember this now.**

## Working Locally

Working on the site locally takes a bit more effort, but it lets you preview your work before publishing. These instructions are skeletal, and assume some familiarity with the tools involved. If you are not familiar with these tools, ask a friend! Learning in the company of others is always better.

### Install Docker

First, [install Docker](https://docs.docker.com/get-docker/). 

### Check out the site

You might prefer GUI tools, in which case [Github Desktop](https://desktop.github.com/) is your friend. Or, you might prefer the command line.

```
git clone git@github.com:state-officer-md/state-officer-md.github.io.git
```

You may have to set up [SSH keys and the like](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account) first; again, these details are beyond the scope of this document.

### Preview!

You should have everything you need to preview the site. (Ha! The truth is, you'll probably have to debug weird 12 things, and it will be frustrating... but, that's just technology.) If you're working from the command line, change into the directory you checked out from git, and do the following:

```
docker-compose up
```

This should pull the appropriate images from Docker, and spin up a container that will build and preview the site. When it is done, head over to your favorite web browser, and go to [http://localhost:4000/](http://localhost:4000/).

(If you're using the Docker Desktop... I have no idea how to use it. Someone might want to update this document with information about that, if it turns out to be possible...)

### Edit! 

This site was largely written in [VS Code](https://code.visualstudio.com/). You might like [](Atom), or [](Sublime Text), or some [other](https://www.vim.org/) [text](https://www.spacemacs.org/) [editor](https://notepad-plus-plus.org/).

Point being, you need a plain text editor. If you're working from the command line on a Mac, and you have VS Code installed (including the shell extensions), you can type:

```
code . 
```

when you're in the repository, and VS Code will open with everything therefore you to edit. 

When you're done editing, you can pop over to your browser and preview your work. You probably have to reload pages to see what you've done.

### Commit!

When you're happy with your work, you can commit your work. 

```
git commit <files that you changed>
```

And, when you're ready to send it live...

```
git push origin main
```

which will send things over the interwebs to Github. The site will then render, and become visible/live.

#### What about staging?

You could, if you want, have a "staging" branch. 

```
git branch staging
git checkout staging
```

Now, you can edit locally, preview locally, and commit/push... and nothing will happen to the live site. When you're ready to make all of your changes "public", you will need to [merge "staging" into "main"](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging):

```
git checkout main
git merge staging main
```

If you're not familiar with `git`, it's OK. There's only three experts on git in the world, and everyone else is just pretending to understand it. Definitely don't ask one of the experts... if you're stuck, [ask a friend](https://18f.gsa.gov/).  

## Handling Errors

It is possible that the GH Pages [build will fail](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/about-jekyll-build-errors-for-github-pages-sites). If so... whee! It's probably a Liquid error, meaning you got some syntax wrong somewhere. However, if your site previewed correctly locally, it is unlikely that it will push-and-fail. Anything that renders correctly locally should render correctly remotely.

# About the Site

Everything that came before was mechanics... the "how" of working with the site. This is the "what" and "why."

The entire site is [a Jekyll site](https://jekyllrb.com/). This is an open source framework for generating static websites. If you are familiar with Jekyll, this site will look fairly tame. If you are not familiar with Jekyll... welcome! It is widely used at 18F, and around the world. The Jekyll site is a great place to learn more, and googling for most anything regarding jekyll will turn up lots of resoureces.

## _data

In the `_data` folder are three critical files.

* `navigation.yaml` defines the menus at the top of every page.
* `resources.yaml` is where we recorded all of the resources used throughout the courses. There is an include that we then use to pull data out of this file. Think of this... as a "link database."
* `rubric.yaml` defines the Health Rubric. It is also used everywhere rubric dimensions are rendered. Modifying this file has significant implications... so, with deference to SNL, *do not taunt the happy fun rubric*. (In truth, this should not need editing.)

## _includes

Includes are a way of defining text/HTML/code once, and then re-using it throughout the site. 

* `airtable-post` and `airtable-pre` generate the includes for linking to the Airtable pre-content and post-learning surveys.
* `alert` is used to generate pop-out alerts on lesson pages.
* `breadcrumbs` is used to generate a breadcrumb element that shows up in some lessons.
* `countdowntimer` is used throughout the lessons to create the cute Javascript countdown timers.
* `course_lesson_list` generates the list of lessons for a course overview page.
* `course_lesson_summaries` then embeds the overviews from each rubric lesson, and the dimensions themselves. Used on course overview pages.
* `indicator` is used in the course content overview.
* `link` is used to reach into `resources.yaml` and extract links. This is used everywhere. Change cautiously.
* `resources` is used to render out sections of the resources page.
* `rubric` renders out a dimension from the rubric itself, given a designator.

Changing any of these will change content all over the site. Be careful when doing so.

## _layouts

These are the scaffolds for every page on the site. Content is flowed into them. Changing these changes the look and feel of the entire site, potentially.

`widepage` is used throughout the site for many of the pages.

## assets

All images, CSS, Javascript, and the like live here.

## collections

There are three Jekyll collections in this site, currently. 

* `_courses` are where course one, two, three, etc. are defined. These have almost no "content" in them... because they reference out to the rubric lessons. They provide the structure of a course, but not the content itself.
* `_rubric` is where there are lessons supporting the rubric. Each dimension has one or more lessons associated with it. Those lessons are then woven together to form courses.
* `_pages` are other static pages on the site. For example, the Joel Test content and Agile practices overview are both examples of static pages.

## .gitignore

This file tells git what not to put into version control. Probably safe to leave it as-is. 

## CNAME

This is where you should put the DNS entry that the site will "live" at. It suggests that a CNAME entry has been created on the appropriate DNS server, and it redirects to `state-officer-md.github.io`. The [github documentation on this should be considered authoritative](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/configuring-a-custom-domain-for-your-github-pages-site).

## docker-compose.yml

This lets you run and preview the site.

```
docker-compose up
```

See the first half of this document...

## LICENSE

Our work, as employees of the federal government, is free for all. Any future contributions should be made under the same license. This includes individuals as well as vendors; all contributions, edits, etc. will become CC0/public domain upon offering.

# That's It.

There is always more to be said, but it will not be said here. 