# Blog Site

An example blog site generated via [Hugo](https://gohugo.io/). It uses a pre-made theme [Bleak](https://themes.gohugo.io/bleak/).

Here is what we get:

![image](https://user-images.githubusercontent.com/8188/38143986-f38eb3c8-3410-11e8-9fc6-72b8212614b9.png)
_Figure: Home Page_

![image](https://user-images.githubusercontent.com/8188/38144029-21a7c22c-3411-11e8-8add-9fd6cfa1c065.png)
_Figure: Single Post Page_

![image](https://user-images.githubusercontent.com/8188/38144088-6628a010-3411-11e8-8dcc-fc97c27a5be5.png)
_Figure: Tags in the footer_

## Pre-requisites

Install Hugo:

```
$ brew install hugo
$ hugo version
```

## Site Creation

```
$ hugo new site sls-blog
```

### Add Theme

```
$ cd sls-blog
$ git init
$ git submodule add https://github.com/Zenithar/hugo-theme-bleak.git themes/bleak

# Edit your config.toml configuration file
# and add the Bleak theme.
echo 'theme = "bleak"' >> config.toml
```

## Content Creation

Add posts:

```
$ hugo new post/my-first-post.md
```

Add any static files i.e. `html`, `css`, `js`, images etc. to the `static` folder. These files will be copied to the destination folder as-is.

## Configuration

To configure the site, edit the `config.toml` file as follows:

```
# baseURL = "http://sls-comps.example.com/"
languageCode = "en-us"
title = "The Serverless Components"
theme = "bleak"
publishDir = "~/projects/prototype-v2/serverless-components/examples/blog/site"

[params]
  Subtitle = "easy, composable, open, serverless components"
  cover = "/images/serverless-components.gif"
```

## Running the site

In development mode, you can run a local server to test your site:

```
$ hugo server -D
```
The site will be available at: `//localhost:1313/`

Once satisfied with the site, generate the static files at a specific destination location by:

```
# To generate files to the default destination folder `public`
$ hugo

# To generate files to a specific destination folder
$ hugo -d ~/projects/prototype-v2/serverless-components/examples/blog/site
```

The generated static files can be deployed to any host.
