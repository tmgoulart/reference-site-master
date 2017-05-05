---
layout: wmt/docs
title:  Images
---
<style>
button.button-img {
border: none;
background: none;
}

.modal-content {
margin: auto;
top: 50px;
width: 50%;
height: auto;
padding: 50px;
}

</style>

# {{ page.title }}

There are different ways to handle images, as mentioned in the
[Markdown Guidelines](/docs/getting-started/markdown-guidelines.html) page.

For the usage of images you have to combine your knowledge about links.

With markdown syntax: 

![Alison Loney]({{ site.baseurl}}/assets/img/team/ali.png)

Or HTML syntax. This allows you to add more tweaks such as sizing.

<img src="{{ site.baseurl}}/assets/img/team/placeholder.png" alt="Placeholder" 
description="This is not Manfred" width="200" height="200"/>


## Thumbnail Images

You can use a thumbnail image as button to expand and see it in a larger
modal. Use HTML to set the width and height of the thumbnail using % and place
the image in the content of the modal for a larger view.

<!-- Trigger/Open The Modal -->
<button type="button" class="button-img" data-toggle="modal" data-target="#myModal">
  <img src="/assets/img/still-here.png" class="img-responsive" width="15%" height="15%" />
</button>


<!-- The Modal -->
<div id="myModal" class="modal">

  <!-- Modal content -->
  <div class="modal-content" id="myModal">
    <img src="/assets/img/still-here.png" class="img-responsive center-block" />
  </div>

</div>

If you have multiple modals on a page, be careful about naming the `data-target`
and the `id` of the modal.

<!-- Trigger/Open The Modal Still Here -->
<button type="button" class="button-img" data-toggle="modal" data-target="#stillHere">
  <img src="/assets/img/still-here.png" class="img-responsive" width="15%" height="15%" />
</button>

<!-- Trigger/Open The Modal Team -->
<button type="button" class="button-img" data-toggle="modal" data-target="#team">
  <img src="/assets/img/team/placeholder.png" class="img-responsive" width="40%" height="40%" />
</button>

<!-- The Modal Still Here -->
<div id="stillHere" class="modal">

  <!-- Modal content -->
  <div class="modal-content" id="stillHere">
    <img src="/assets/img/still-here.png" class="img-responsive center-block" />
  </div>

</div>

<!-- The Modal Still Here -->
<div id="team" class="modal">

  <!-- Modal content -->
  <div class="modal-content" id="team">
    <img src="/assets/img/team/placeholder.png" class="img-responsive center-block" />
  </div>

</div>

