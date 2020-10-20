---
layout: default
title: Home
nav_order: 0
description: "3D printing Wiki"
permalink: /
last_modified_date: 2020-07-31T17:54:08+0000
---

This wiki is a FAQ page for our 3D printing group: [@Print3D_Group](https://t.me/Print3D_Group)

Feel free to add pages or update content, edit the files on GitHub and send a pull request.

The content is licenses under the [Creative Commons CC0 license](https://github.com/Depau/3dprint-wiki/blob/master/LICENSE).


## Contributing content

All pages are under the [`/wiki`](https://github.com/Depau/3dprint-wiki/tree/master/wiki) folder.

You should check out the [Kramdown Markdown reference](https://kramdown.gettalong.org/quickref.html) to
learn how to write markdown pages that work well on the website.


### Markdown cheatsheet

````markdown
# Title

## Section title

### Paragraph title

#### Subparagraph title

↑ Titles go on their own line. Add a blank line after each title, and two (but at least one) before

This is **bold**, *italic* and ~~strikethrough~~, while this is some short `code sample`.

```python
A larger code sample can be enclosed within three backticks,
like this. You can also set the programming language. 
```

- this is
- a bulleted list

1. this is
2. a numbered list

[External link text](https://some.website)
{% raw %}[Internal link text]({{ '/wiki/software/slicer' | absolute_url }}){% endraw %}

![External image description](https://some.site/picture.png)

Icons from ForkAwesome: https://forkaweso.me/Fork-Awesome/icons/
Just paste the code from the icon page, for example:
<i class="fa fa-archlinux" aria-hidden="true"></i>

There's a shortcut for Wikipedia links:
{% raw %}{% include wiki %}{% endraw %}
````


### Edit an existing page

Just open the page file on GitHub and click the "pencil" icon to edit it.

On the website you will find a "Edit this page on GitHub" button around the bottom of the page.


### Creating a new page

In the wiki folder, click "Add file", "Create new file".

The file name ends up in the URL: it should be something like `page-name.md`, the URL
will be `/wiki/page-name`.

Paste and adjust the following content at the beginning of the file to set the
page layout and the title, then add the content after that.

```yml
---
layout: default
title: Page title
#parent: Parent title if this is a sub-page, otherwise delete this line
#has_children: true if this page has children, otherwise delete this line
---

# Page title
```

### Navigation

Documentation on the site navigation can be found [here](https://pmarsceill.github.io/just-the-docs/docs/navigation-structure/#main-navigation).

### Uploading pictures

To avoid making the repository overly big, just upload them to [postimages.org](https://postimages.org/)

## Testing the website on your computer

- Install Docker for Linux or macOS (it should work on Windows too but the command needs to be adapted)
- Clone the Git repository to your computer
- Run the website on your computer by running on the terminal:

```bash
docker run --rm --volume="$PWD:/srv/jekyll" -p 4000:4000 -it jekyll/jekyll jekyll serve
```

- The website will be available at [localhost:4000](http://localhost:4000)
