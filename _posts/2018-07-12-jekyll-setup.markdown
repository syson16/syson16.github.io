---
layout: post
title:  "Start a Blog with Jekyll and Github Pages"
date:   2018-07-12 00:00:00 -0600
categories: jekyll update
---

# Start a Blog with Jekyll and Github Pages

For this tutorial, I assumed that Homebrew is installed on your mac os machine.

## Install the latest Ruby version via Homebrew

```
# Check the ruby version
ruby -v

# Install the latest ruby
brew install ruby

# Restart your terminal
ruby -v
```

## Install Jekyll

```
# Install Jekyll and Bundler gems through RubyGems
gem install jekyll bundler

# Create a new Jekyll site at ./myblog
jekyll new myblog

# Change into your new directory
cd myblog

# Build the site on the preview server
bundle exec jekyll serve

# Now browse to http://localhost:4000
```

## Host it on Github pages

**You don't need to build it** before you push it to the Github repository. Github will generate the static files for you. 

### User or organization site
*From [<https://pages.github.com/>](https://pages.github.com/)*

#### Create a repository

Create a new repository named *username*.github.io, where *username* is your username (or organization name) on GitHub.

e.g.

> your id: `yuzutea`
> 
> repository name: `yuzutea.github.io`


If the first *username* part(*username*.github.io) of the repository doesn’t exactly match your username, it won’t work, so make sure to get it right.

#### Push it

```
# Clone the repository
git clone https://github.com/username/username.github.io

# Create a new Jekyll site at ./username.github.io
jekyll new username.github.io

# Add, commit and push your changes

git add --all
git commit -m "Initial commit"
git push -u origin master

```

#### Done
Go to *username.github.io* on a browser. Please allow a few minutes for the blog to go live.

### Project site

Follow the same steps as the user/organization site but the url will be different. *username.github.io/repository*.