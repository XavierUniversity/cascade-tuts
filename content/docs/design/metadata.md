---
title: 'Metadata Sets'
date: 2020-04-15T19:27:37+10:00
weight: 2
---

Metadata Sets represents a curated collection of metadata fields used to describe content.

<!--more-->

- [What are Metadata Sets?](#what-are-metadata-sets)
- [Creating a Metadata Set](#creating-a-metadata-set)

---

## What are Metadata Sets?

Metadata is data that describes an asset. This can be as simple or as complicated as 
desired for the use case. In the Xavier use case, we do our best to simplify this set
across the entire site (including folders, files and pages). 

While there are a number of built-in fields that include: 

- Name (display name, title) 
- Summary (teaser, summary, description)
- Keywords
- Author
- Dates (start, end, review)
- Expiration Folder

We can also define some custom fields. We currently use 3 custom fields in our
default metadata set. These are mainly used for pages and/or folders.

- Show in Navigation - shows/hides a page from the navigation menus on a content site, or other dynamic navigation areas
- Require Authentication - locks the page behind a user login
- Hide from Search Engine - includes a no-follow meta tag

### Xavier Example:

Our Default Metadata Set includes the three custom fields outlined above and also shows the following fields:

- Display Name, Title, Keywords, and Description

All other fields are hidden, as we do not intend to use them in our basic pages.

## Creating a Metadata Set

1. Navigate to Manage Site > Metadata Sets and click Add. You may also want to add a new
container, depending on the architecture desired.
2. Enter the Name and select the Parent Container, as desired.
3. Identify which built-in fields you'd want to use and define any of the following:
  - Help Text
  - Visibility - Determines where a field is shown. Inline = Content Tab; Visible = Shown on Metadata tab; Hidden = Not shown.
  - Required
4. Define any Custom fields you would want to display.
5. Preview & Submit!