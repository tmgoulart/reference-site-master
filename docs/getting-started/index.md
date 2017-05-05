---
layout: wmt/docs
title: First Steps
---

<img src="/assets/wmt/img/icons/internal/icon-gettingStarted.png" width="150" height="150" alt="getting started" align="right"/>

# {{ page.title }}
  
So you want to create your own site based on the WMT reference site?
Great. Let's get started.

## Prerequisites

Maintaining your own site with WMT and Jekyll is easy and can be learned
quickly. At a minimum you will need to know a bit of

* Git
* Markdown
* Jekyll

More advanced usage is aided by knowledge of

* HTML
* CSS
* Bootstrap
* Liquid
* JavaScript

and others.

## Creating your Site

A number of simple steps are needed to start your site.

1. Create a git repository for your own site - e.g. `my-team-site`
2. Download the
   [reference site source as a zip file](https://gecgithub01.walmart.com/devtools/reference-site/archive/master.zip).
3. Unzip the archive into the cloned directory.
4. Commit and push all the files. Optionally remove files you dont want to use.


Now your are ready to test your site locally

```
jekyll serve
```

Navigate to [http://localhost:4000](http://localhost:4000). The site should look
identical to the deployed reference site at
[http://reference.walmart.com](http://reference.walmart.com) - or at least
similar to it if we have updated the site since you created the zip.

Now you are ready to adapt the site to your usage.

- Update the `_config.yml` properties file for your site
- Add a file `wmt-release-id.txt` containing the current date, this will help
  with updates later
- Update the logo images `assets/img/logo.jpg` and `assets/img/homeBanner.png`
- Create new pages based off existing ones and check out the more about
[page types](./page-layouts.html)),
[writing in general](./writing-guidelines.html) and
[markdown specifically](./markdown-guidelines.html)
- Remove pages you do not want
- Update the navigation in `_config.yml` and potentially
  `_includes/docs-navigation.html`
- Check out the included icons, buttons, colors and more in the
  [base styles section](./base-styles/index.html)

After reviewing the linked section you might want to learn more about the
technologies used under the hood or some
[advanced usage](../advanced/index.html).
