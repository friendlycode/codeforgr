---
title: Submitting a Blog Post
layout: resource
type: guide
edit_link: https://editfordc.herokuapp.com/document/f37eceab-5a56-41b4-ba19-2e90e29a60e1
---

# How to Make a Blog Post

The Friendly Code blog is open for contributions for the community. Here's how you do it:

## Propose your post

Before you start, you may want to run your idea by [us](/contact.html) to make sure that it is a good fit for the blog.

## Fork the website repo

If you haven't already, go to the [site's repo](https://github.com/codefordc/codefordc-2.0) and make your own fork. This is your personal copy to do as you wish, and nothing will affect the public site until your changes are merged into the original repo (see below).

## Create a new file for your post and add your avatar

In a Jekyll site like Friendly Code's, blog posts live in the `blog` folder. There are two folders there: `_drafts` and `_posts`. If you were working on a live version of the site, you'd use the `_drafts` folder to hide your post until it was ready, but since you're on a separate fork you should just work in `_posts`.

Create a new file in `_posts`, with the name `yyyy-mm-dd-your-post-title`. You can use either the `.md` or `.html` file extension, depending on whether you wrote your post in Markdown or HTML.

Your author information will live in the _data/blog_authors.yml file. Choose a unique name and set the info you'd like to share. We suggest including at least a Twitter username. You'll be able to use that name on any post, and we'll automatically populate your information into the post.

## Write your post

Certain things, like the title, author info, and post time, are set in what's called the YAML front matter at the top of the post. It looks something like this:

    ---
    layout: post
    title:  "Your Blog Post Title"
    authors:
    - yourname
    date:   yyyy-mm-dd hh:mm:ss
    categories: blog
    image: "path/to/image.jpg" #optional
    description: "A very brief summary of the post" #optional
    ---

For the date field, choose the date that you'd want your post to go up. If you don't have a preference, just put the current date. Make sure that it matches the date in your filename.

Then, you just need to type up the body of your post. If you'd prefer to set an excerpt for the main page other than the first 50 words, pop a `<!--more-->` tag in where the excerpt should cut off.

## Check your work and open a pull request

Once you've committed your post to your fork of the repo, run jekyll and check that everything looks good:

jekyll serve --watch --future

Point your browser to localhost:4000/blog to see your handiwork. When you're ready, open a pull request from your fork to the Friendly Code repo. We'll review the post and, if everything is good to go, we'll merge it in and you're done!
