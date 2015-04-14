---
---
# Bestbrains DNA-WIP - tech setup for the site

Bestbrains DNA is a web site that describes how Bestbrains (will) works and why. The source lives on github and is auto-published on [http://dna-wip.bestbrains.dk](http://dna-wip.bestbrains.dk) every time a change is pushed.

Below are instructions for how to set up a local development environment. Useful for when you want to make many changes and test locally before pushing to github. See [How to clone](http://dna-wip.bestbrains.dk/docs/how-to-copy.html) for more options on how to clone the Bestbrains model.


## 1. Install GIT

Here's [how to install GIT](http://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

## 2. Clone the repo

Tell git to download the bestbrains-dna source:

    git clone https://github.com/bestbrains/bestbrains-dna.git
	cd bestbrains-dna

You should now have the whole thing, including the README.md file that you are reading right now!

The web site source files are under _docs, have a look! They are written using [textile](http://redcloth.org/textile) (a simpler format than html). When you push to github, it will automatically convert the pages to static html and build the site http://dna-wip.bestbrains.dk.

## 3. Install Jekyll and related tools

To test the site locally, you need to install jekyll (the tool that github uses to generate sites), which in turn relies on some Ruby stuff. But you can do all easily via Ruby bundler, like this:

First install Ruby if you don't already have it, for example via [homebrew](http://brew.sh).

    brew install ruby

Then install the Ruby Bundler gem, if you don't already have it.

    gem install bundler

Next, tell the bundler to install all the gems needed (jekyll, github-pages, etc). They are listed in Gemfile in case you are curious.

	bundle install

Congrats! You got the stuff you need. You should now be ready to....

## 4. Run the site locally!

Tell Jekyll to generate the site and serve it up:

    jekyll serve

Or if you are lazy you can use the run script (which just does jekyll serve)

That's it, your local copy of the Bestbrains DNA site should be up and running on
[http://localhost:4000](http://localhost:4000)

Every time you edit a source doc (under _docs) it will update the site automatically.

## 5. Bestbrains process
Right now, we agreed to do trivial changes (replace Crisp with Bestbrains in the places where they talk about the company that the site is about, but not in the places where they talk about how they came up with it all).

At the same time, identify places where you would propose that we make other changes (because that would be more right for Bestbrains). We add them inline in the documents, clearly marked. 

I created such a proposal at the top of what-is-bestbrains.textile - this is then clearly marked in the css.

Bo also created a new page, things-we-need-to-decide, add to that too.
