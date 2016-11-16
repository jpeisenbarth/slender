Slender
=======

Minimalist theme for [Hugo](http://gohugo.io/) with [base16](https://github.com/chriskempson/base16) color schemes.

It is based on the work of CrimsonRay. I reupload this on github because CrimsonRay's account cannot be found anymore and thus it is impossible to find the Slender theme repository anymore.

[Demo](http://eisenbarth.io)

### Screenshot

![screenshot](https://raw.githubusercontent.com/Eisenbarth/slender/master/images/screenshot.png)

### Features

* Responsive
* Pagination
* [base16](https://github.com/chriskempson/base16) color schemes
* Code/syntax highlighting with [highlight.js 9.0.0](https://highlightjs.org/)
* Social links with [FontAwesome 4.5.0](https://fortawesome.github.io/Font-Awesome/)
* Google Analytics integration
* Proper meta tags for SEO

### Color Schemes

![slender-color-schemes](https://raw.githubusercontent.com/Eisenbarth/slender/master/images/slender-color-schemes.png)

### Installation

1. Make a new Hugo site

    ```none
    hugo new site my_site/
    ```

2. Install Slender ans set up your site

    ```none
    cd my_site/
    git clone https://github.com/Eisenbarth/slender themes/slender
    cp -a themes/slender/exampleSite/* .
    ```

### Configuration

```toml
# config.toml
# https://github.com/Eisenbarth/slender

baseurl = "http://url-to-your-site.com/"
title = "Your Title"
languageCode = "en-US"
MetaDataFormat = "toml"
theme = "slender"
paginate = 3
PaginatePath = "/"

[author]
    name = "Your Name"

[permalinks]

    # Permalink format for pages.
    page = "/:title/"

    # Permalink format for blog posts.
    post = "/article/:title/"

[params]

    # Change the color scheme of Slender.
    # See above for preview and list of color schemes.
    colorscheme = "white"

    # Tagline; HTML accepted here. Keep it concise.
    tagline = "Your Tagline"

    # Footer; Markdown accepted here.
    footer = "Copyright 2015 &copy; Your Name"

    # Description and keywords for <meta> tags.
    # Remember to set this for your main page.
    # This will be overridden by whatever is set by the page or post,
    # defined by `description` and `keywords` variables in the front matter
    # of the markdown file.
    description = "Default Page Description"
    keywords = "default,page,keywords"

    # Social links, must be full URLs (e.g. https://github.com/Eisenbarth/).
    # Remove, comment, or leave blank any field to leave them out.
    email = "mailto:your-email"
    github = "url-to-your-github"
    bitbucket = "url-to-your-bitbucket"
    twitter = "url-to-your-twitter"
    stackoverflow = "url-to-your-stackoverflow"
    linkedin = "url-to-your-linkedin"
    facebook = "url-to-your-facebook"

    # Google Analytics
    # Remove, comment, or leave it blank if you don't have one.
    ganalytics = "your-google-analytics-tracking-code"

[menu]

    # Menu for the nav bar.
    # There must always be one item present (e.g. home).
    [[menu.main]]
    identifier = "home"
    name       = "home"
    url        = "/"
    weight     = 0

    [[menu.main]]
    identifier = "about"
    name       = "about"
    url        = "/about/"
    weight     = 1
```

### Usage

**Making a new post / article**

```none
$ hugo new post/hello.md
```

**Making a new page**

```none
$ hugo new page/about.md
```

Add the new page to navbar in `config.toml` under `[menu]`.

### Launch The Hugo server

    ```none
    hugo server
    ```

### License

[MIT](LICENSE.md)
Original work &copy; 2015-2016 CrimsonRay
Modified work &copy; 2016 Eisenbarth
