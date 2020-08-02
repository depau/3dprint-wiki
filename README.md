# 3D printing wiki

Wiki/FAQ based on contributions from the 3D printing Telegram group: [@Print3D_Group](https://t.me/Print3D_Group)

- Theme: https://github.com/pmarsceill/just-the-docs, MIT-licensed.
- Content: Creative Commons CC0 1.0 Universal License - Public domain

https://creativecommons.org/publicdomain/zero/1.0/legalcode.txt


## Contributing content

All pages are under the [`/wiki`](https://github.com/Depau/3dprint-wiki/tree/master/wiki) folder.

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
nav_order: 2
---

# Page title
```

### Uploading pictures

To avoid making the repository overly big, just upload them to [postimages.org](https://postimages.org/)
