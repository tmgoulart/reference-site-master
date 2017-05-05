---
layout: wmt/docs
title:  Markdown Guidelines
---
 
# {{ page.title }}

In general all content should be authored in Markdown as outlined in
[the documentation guideline](./writing-guidelines.html). This page serves as an
example page for writing with Markdown and how it ends up looking. You also find
some further tips and tricks about using Liquid and HTML. Beyond that e.g. have
a look at
[the GitHub docs](https://help.github.com/articles/basic-writing-and-formatting-syntax/)
about markdown..

So let's get started.

# General

Titles are marked with one or more `#`.

# Level 1

## Level 2

### Level 3

#### Level 4

##### Level 5

###### Level 6

Always use Level 1 for the page title and also for other important titles on a
specific page. Also keep in mind that while up to Level 5 work on the site, it
nearly never makes sense to nest a document that deeep. If you need more than
Level 3 you should probably think about reorganizing your content.

Normal writing is just done in paragraphs. Ideally keep the markdown source code
formatted to use hard breaks so that usage in various editors and also in GitHub
and other systems is easier. We suggest a margin of anywhere from 80 to 120
characters.

User interface labels and elements should be highlighted with underscore
(italics):

Once you have added all the details, press the _Apply_ button.

If you want to put specific importance on a word or phrase use double underscore
(bold):

Do __NOT__ write all your pages in straight up __HTML__. Instead __use
markdown__ whenever possible!

In some cases it can be useful to go beyond that and combine italics and
bold. Just replace usage of `_` with `*`. So it could end up *__looking like
this__*.

To highlight a whole paragraph you can use a blockquote by add a `>` at the
start of each line

> _Warning:_  
>  
> Do not use block quotes too often.


# Input Values and Source Code

When specific values are mentioned they should be highlighted in the same
fashion as source code elements:

You can see a directory listing of the `foo` folder by using the `ls` command on
Unix operating systems.

For longer command line examples it is best to have them in a separate source
code block. The markdown syntax uses three back-ticks.

```
cd /opt/dev/myproject
mvn clean install
```

You can also a specific language like `shell` after the three backticks to get
syntax highlighting.

```shell
cd /opt/dev/myproject
mvn clean install
```

# Lists

In general, lists are very useful - but be careful not to overuse them.

## Ordered Lists

Numbers in the source code don't matter. They will be computed. So you can use
e.g. 1. all the time.

1. Item 1
1. Item 2
    1. Nested 1 (nested items in lists require 4 spaces to indent properly)
    1. Nested 2
1. Item 3

## Unordered Lists

Use `-` or `*` for the items.

- Apple
- Pear
- Banana

You can also indent:

- Pets
    - Dog
    - Cat
- Farm animal
    - Cow
    - Sheep

## Combined Lists

You can combine ordered and unordered lists items.

1. You
1. can 
    2. combine
    * unordered
    * and
2. ordered
3. list
    * items.

## Definition List

Just use [dl/dt/dd HTML](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl). 

# Links


By default the markdown syntax with `[text](url)` should be used. Relative links
are preferred to avoid issues with the root context.

If you perfer to use absolute links, we recommend that you add usage of the
`site.baseurl` property via Liquid tags. For adding further behavior like
`target="_blank"`, just fall back to using HTML instead of markdown.

Here are a few links with different syntax to the same page:

* Simple relative link using markdown:
  [Writing Guidelines](./writing-guidelines.html)
* Simple relative link using HTML with added target: <a  href="./writing-guidelines.html" target="_blank">Writing Guidelines</a>
* Absolute link with baseurl using markdown: 
  [Writing Guidelines]({{ site.baseurl }}/docs/getting-started/writing-guidelines.html)
* Absolute link with baseurl using HTML: 
  <a href="{{ site.baseurl }}/docs/getting-started/writing-guidelines.html" target="_blank">Writing Guidelines</a>

When validating your site it can be very useful to use the link validation tools
like [Linkchecker](http://wummel.github.io/linkchecker/). An example script
`linkcheck.sh` for local development check is part of this project in the
`_tools` folder.

# Images

For the usage of images you have to combine your knowledge about links from
above ...

With markdown syntax:

![Alison Loney]({{ site.baseurl}}/assets/img/team/ali.png)

Or HTML syntax. This allows you to add more tweaks such as sizing.

<img src="{{ site.baseurl}}/assets/img/team/placeholder.png" alt="Placeholder" 
description="This is not Manfred" width="200" height="200"/>

# Tables

Generally you should not use too many tables in any document, but when you
really need one you can use markdown syntax:

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

There must be at least 3 dashes separating each header cell.  The outer pipes
(|) are optional, and you don't need to make the raw Markdown line up
prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3


Or get fancier with raw HTML.

<table width="50%">
<tr>
<th>First Name</th>
<th>Last Name</th>
</tr>
<tr>
<td>Alison</td>
<td>Loney</td>
</tr>
<tr>
<td>Manfred</td>
<td>Moser</td>
</tr>
</table>
