---
layout: wmt/docs
title:  Page Layouts
---
 
# Page Layouts

A number of page layouts are included with the site. All of them can be used by
defining `layout: name` in the front matter of a document.

## Default

The `default` layout is the simplest template and the base for all others. It is
used on the [about page]({{ site.baseurl }}/about.html) and can be used as
template for any other desired templates on your own site.

Source:
- `_layouts/default.html`

Examples:
- `about.md`

## Home

The `home` layout is template for index pages that are meant to use full width
of the browser window with a banner. It is used on the [index page]({{
site.baseurl }}).

Source:
- `_layouts/home.html`

Examples:
- `index.md`

## Projects

The `project` layout is a modified version of the default that automatically
uses the page title from each projects page for added consistency and changes
the overall page width. It is used for the [Projects section]({{ site.baseurl
}})

Source:

- `_layouts/project.html`

Examples:

All files in the `projects` folder including the index page.

## Docs

The `docs` layout includes a number of features that make it very useful for
multi-page documentation for a specific topic. It is used for the
[Docs section]({{ site.baseurl }}/docs/index.html) on this site, but can be used
for multiple documentation or similar sections on a site as long as separate
contexts and include files are used. It contains the following features:

- Left hand navigation
- Edit page source link
- Breadcrumb navigation for improved navigation between linked content

Source:

- `_layouts/docs.html`

Examples:

All files in the `docs` folder including index pages.

## Blog

The `post` layout powers the rendering of every blog post. It works together
with the `default` layout used in the [Blog]({{ site.baseurl }}/blog/) section
index page to render a list of posts and the individual posts.

Features included are

- Date of post rendered in page from post file name
- Post title from post front matter
- Post authors from post front matter and global config

Source: 

- `_layouts/post.html`

Examples:

All files in the `blog` and `_posts` and `_drafts` folders.

Blog posts have to use the file naming pattern as the existing posts using date
and title. The front matter can include a `published` flag.

You can deactivate blog usage on the site by removing the blog link from the top
navigation in `_config.yml`. If desired, you can also remove the `blog`,
`_posts` and `_drafts` folder
