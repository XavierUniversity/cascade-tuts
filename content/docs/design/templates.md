---
title: 'Templates'
date: 2020-04-15T19:27:37+10:00
weight: 1
---

Templates are the lifeblood of building sites and structures within Cascade. They
are XHTML documents that provide the basic page structure. 

<!--more-->

- [System Tags](#system-tags)
- [Configuration](#configuration)

---

Templates typically contain the basic HTML scaffolding and necessary scripts and styles
to produce the desired look and feel of a page.

Templates can be created by clicking `Add Content > Default > Template`.

The most basic template must include the following `system-tag`.

```
  <system-region name="DEFAULT" />
```

Templates can be as sophisticated or simplistic as needed. System tags are used 
to define areas of need within a specific page design. For instance, if you wanted
a main content area and a sidebar the following could be used:

```html
<html>
  <head><!-- head code --></head>
  <body>
    <div class="main">
      <system-region name="DEFAULT"/>
    </div>
    <div class="sidebar">
      <system-region name="SIDEBAR"/>
    </div>
  </body>
</html>
```

This code would provide some layout while also allowing multiple formats to be used
to define the various components.

## System Tags

System tags may be used to define various content areas. `DEFAULT` is required by all templates
and can be static, dynamic, or a result of a format acting on a block.

System tags may also be used for metadata tags (e.g. title, author, etc).
Available Tags:

- **Content Regions**
  - `<system-region name="DEFAULT|CUSTOM_NAME" />` - Any user defined region. `DEFAULT` is a required element of all templates
- **Page Name(s)**
  - `<system-page-name/>` - system name of the page asset (computer-name)
  - `<system-page-title/>`- user defined Title
  - `<system-page-display-name/>` - user defined Display Name
- **Other Metadata**
  - `<system-page-author/>` - page author, from the metadata field. Not necessarily the Cascade User
  - `<system-page-summary/>` - user defined summary
  - `<system-page-teaser/>` - user defined Teaser, from the metadata field
  - `<system-page-description/>` - user defined description
  - `<system-page-keywords/>` - user defined Keywords
  - `<system-page-start-date/>` - page's start date
  - `<system-page-end-date/>` - page's end date
  - `<system-page-meta-date/>` - current time when the page is rendered
- **Helpful Meta Tags** - This code, when used in a Template, will render the full `<meta name="keywords|description" content="CONTENT" />` code
  - `<system-page-meta-description/>`
  - `<system-page-meta-keywords/>`

[Cascade Docs](https://www.hannonhill.com/cascadecms/latest/content-authoring/pages/system-tags.html)

## Configuration

After defining custom `system-region`s you can then configure the template to use
formats and blocks to render static, dynamic or function-based content.

[Configurations](/docs/configurations) can also represent one or more outputs that are used to display page content.