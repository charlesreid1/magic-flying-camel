# magic flying camel

Walkthrough of how to get a simple Jekyll Github Pages 
page all set up.

## How it works

Let's cover how this all works first, before we cover the steps.

You'll start by copying the `docs/` folder from this repository
into the `docs/` folder of your repository.

This folder contains the "source" of your static website - 
the plain markdown files and HTML templates that are used
to assemble the final page's static content.

Github Pages does the actual work of assembling the 
static content. It offers this service for free,
if you agree to use Jekyll...

(This sucks you into the JS/Ruby environment. 
Don't do it! It's a trap!)

The `docs/` folder contains some Ruby files that you can use
to configure the site.

## Quick start: no ruby

If you want to avoid using Ruby...

Clone magic-flying-camel somewhere on your hard drive

```
$ cd /tmp
$ git clone https://github.com/charlesreid1/magic-flying-camel
$ cd magic-flying-camel
```

Copy the `docs/` folder to your own repository:

```
$ cp -r docs /path/to/my/repo/docs
```

Although this template is designed for minimal configuration,
there are a few Jekyll settings you will have to set.
These include the site title, github URL, and author info.

These are located in a YAML file: `docs/_config.yml`.

You can add Markdown files to the `docs/` folder and they will
be rendered in the final site. Use magic-flying-camel as an example
of how to create a multi-site static site where things inter-link.

## Hosting locally: with ruby

If you want to brave the confusions of Ruby... 

* On a Mac: Homebrew is recommended. It runs on Ruby.
* On a Linux: aptitude?
* On a something else: good luck, you probably know what you're doing.

This is where things get confusing. 

You'll need `gem`, which is a ruby thing, but different from Ruby, 
because it is used to install things:

```
$ brew install gem

# or 

$ apt-get install gem
```


You'll need `bundle`, which is used to install things, but different from gem:

```
$ gem install bundle
```

Now you need to update your `bundle`:

```
$ bundle update
```

Run `jekyll build` to build the site in `_site` 
(this uses `bundle` to install things):

```
$ jekyll build
```

To view the site locally:

```
$ jekyll serve
```

available now on port 4000!

