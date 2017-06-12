# jekyll-theme-mdui

A Jekyll theme based on mdui

[demo](https://blog.kejun.space) or [docs](http://mdui.kejun.space/#/zh-cn/)

[![Version](https://img.shields.io/badge/version-0.4.1-green.svg?style=flat-square)]()
[![Jekyll](https://img.shields.io/badge/Jekyll-3.4+-green.svg?style=flat-square)](https://jekyllrb.com/)
[![Gem](https://img.shields.io/gem/dt/jekyll-theme-mdui.svg?style=flat-square)](https://rubygems.org/gems/jekyll-theme-mdui/)

[![Code Climate](https://img.shields.io/codeclimate/github/KeJunMao/jekyll-theme-mdui.svg?style=flat-square)](https://codeclimate.com/github/KeJunMao/jekyll-theme-mdui/)
[![Build Status](https://img.shields.io/travis/KeJunMao/jekyll-theme-mdui.svg?style=flat-square)](https://travis-ci.org/KeJunMao/jekyll-theme-mdui)
[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg?style=flat-square)](http://commitizen.github.io/cz-cli/)

[![Author](https://img.shields.io/badge/author-KeJun-blue.svg?style=flat-square)](https://blog.kejun.space)

## Installation

**Now,we have `build` branch ,you can clone this branch to install.**

We have two ways to install themes.

But,**We recommend you use the second ways.**

### First ways

Add this line to your Jekyll site's `Gemfile`:

```ruby
gem "jekyll-theme-mdui"
```

And add this line to your Jekyll site's `_config.yml`:

```yaml
theme: jekyll-theme-mdui
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install jekyll-theme-mdui

### Second ways

Fork this repo to your repo:

```shell
git clone https://github.com/yourname/jekyll-theme-mdui.git
cd jekyll-theme-mdui
bundle install
jekyll s -w
```

Or **direct clone**:

```shell
git clone https://github.com/KeJunMao/jekyll-theme-mdui.git
cd jekyll-theme-mdui
bundle install
jekyll s -w
```

## Usage

### _config

```yml
title: "Jekyll-Theme-MDUI" # Your site title
description: "A Jekyll theme based on MDUI" # Your site description
url: # Your site url
baseurl: # baseurl
author: "KeJun" # Your name

paginate: 5 # paginate
paginate_path: "/blog/page:num/" # paginate path

gems: # paginate gem 
  - jekyll-paginate
```

### _data

* friends.yml
```yml
- name: MDUI # name
  image:  # avatar or logo
  url: https://www.mdui.org/ # url
  describe: 一套用于开发 Material Design 网页的前端框架
``` 
* menus.yml
```yml
- name: SEARCH # name
  url: /pages/menus/search.html # path
  icon: search # icon from https://www.mdui.org/docs/material_icon
```
Default does not display the editor.If you want the editor to appear in the menu:
```yml
- name: Editor # name
  url: /pages/editor.html # path
  icon: edit # icon from https://www.mdui.org/docs/material_icon
```
* sns.yml
```yml
- name: bilibili # name
  url:  # url , if it is empty, it is not enabled
```
Supported:bilibili,facebook,github,gplus,instagram,linkedin,telegram,tumblr,twitter,weibo,zhihu

* **site.yml**
```yml
head: 
   favicon: "https://ooo.0o0.ooo/2017/05/27/59294212bc16e.png" #  the favicon
   high_res_favicon: "https://ooo.0o0.ooo/2017/06/08/5939484dc618e.png" #  the favicon using high quality format
   apple_touch_icon: "https://ooo.0o0.ooo/2017/06/08/5939484dc618e.png" # the iOS Home button icon
   keywords: "blog jekyll mdui theme" #  the site keywords

uiux:
   android_chrome_color: "#eeeeee" #  the color of the Chrome address bar
   nprogress_color: "#29d" #  the color of the top loading progress bar
   nprogress_buffer: 200 # the top loading progress bar buffers

background: 
   purecolor: "#eeeeee" # the background color

img: 
   avatar: "https://ooo.0o0.ooo/2017/05/26/5928368d409dd.png" # your avatar

card: 
   card_shadow: 1 # card shadow (0-24), 0 is not displayed
   card_hoverable: false # When the hover to deepen the shadow

sns_share: # SNS Share Switch
   twitter: true
   facebook: false
   googleplus: false
   weibo: true
   linkedin: false
   qq: true
   telegram: true

disqus:
   disqus_shortname: "" # Your disqus 
   disqus_button: true # disqus load button
   disqus_proxy: false # # disqus proxy(Do not use)
   disqus_proxy_url: "" # (Do not use)
   disqus_api_key: "" # (Do not use)

google_analytics: ""  # google analytics code

lang: "en-US"  # lang
```

### manifest.json
```json
{
  "name": "KeJun BLOG",
  "short_name": "KeJun", 
  "icons": [{
        "src": "assets/images/touch/icon-128x128.png",
        "sizes": "128x128",
        "type": "image/png"
      }, {
        "src": "assets/images/touch/apple-touch-icon.png",
        "sizes": "152x152",
        "type": "image/png"
      }, {
        "src": "assets/images/touch/ms-touch-icon-144x144-precomposed.png",
        "sizes": "144x144",
        "type": "image/png"
      }, {
        "src": "assets/images/touch/chrome-touch-icon-192x192.png",
        "sizes": "192x192",
        "type": "image/png"
      }],
  "start_url": "/index.html?homescreen=1",
  "display": "standalone",
  "background_color": "#fdfdfd",
  "theme_color": "#2a7ae2"
}
```
Replace it with your logo:`assets/images/touch`

### _post

Add the following format to your posts:

```liquid
{% include tips.html content="protips" %}
{% include note.html content="note" %}
{% include warn.html content="warnings" %}
```

[demo](https://blog.kejun.space/living/2017/05/29/jekyll-theme-mdui.html)

## TODO

...

## Note

### file
If you use the first ways to install, you need to download the following files to your jekyll website root directory Or create a new file,And replace it with your own information:

|files|Required or Optional|Description|
|---  |---                 |---        |
|mainifest.json|Optional   |Is the only file that every WebExtension must contain.See [here](https://developer.mozilla.org/en-US/Add-ons/WebExtensions/manifest.json).|
|sw.js|Optional            |Service Workers.See [here](https://developers.google.com/web/fundamentals/getting-started/primers/service-workers).|
|search.json|Optional|If you use the search page, it is required.|
|tags.json|Optional|If you use the tags page, it is required.|
|_data/friends.yml|Optional|If you use the friends page, it is required.|
|_data/sns.yml|Optional|It is footer sns,if you want userd, it is required.|
|_data/site.yml|Required|It is theme config.|
|_data/lang.yml|Required|It is language config.|
|_data/menus.yml|Required|It is site menus config.|

How to use? See Usage.

### service workers

If you use the first ways to install, You will not be able to use service workers!!!!

Why? See `sw.js` content.

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/KeJunMao/jekyll-theme-mdui. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## Development

To set up your environment to develop this theme, run `bundle install`.

Your theme is setup just like a normal Jekyll site! To test your theme, run `bundle exec jekyll serve` and open your browser at `http://localhost:4000`. This starts a Jekyll server using your theme. Add pages, documents, data, etc. like normal to test your theme's contents. As you make modifications to your theme and to your content, your site will regenerate and you should see the changes in the browser after a refresh, just like normal.

When your theme is released, only the files in `_layouts`, `_includes`, and `assets` tracked with Git will be released.

## License

The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
