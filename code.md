---
title: Code
nav_order: 4
layout: home
---

# Main Navigation

The main navigation for your Just the Docs site is at the left side of the page on large screens, and at the top (behind a tap) on small screens.

You need to specify the `title` of each page in its front matter. Page titles are independent of file names and directory structure. The navigation uses the title of the page as an anchor for links to the page.


{: .new-title }
> New (v0.10.0)
>
> The main navigation can be structured as a multi-level menu of unlimited depth:
> pages can always have child pages.

For the construction of the navigation display to work (and to avoid potential confusion when browsing) ***the page titles on your site need to satisfy the following requirements:***

* Top-level pages must have different titles.
* Pages with the same parent must have different titles.
* The title of each page must be different from the titles of all its child pages, and from the titles of their child pages, etc.


