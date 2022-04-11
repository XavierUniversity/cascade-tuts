---
title: 'Blocks'
date: 2018-11-28T15:14:39+10:00
weight: 2
bookFlatSection: false
bookToc: true
---

# Blocks

A block is a piece of content that can be inserted into any page region. This can be 
done with or without styling. This items are commonly used for repeated content.
Such as, an "About" section that appears on every press release. This would
allow the content to be pushed out without managing it in multiple places.

## Types of Blocks

Below is an overview of the types of blocks available for use. Blocks can be used
within Formats via the `LocatorTool` or by assignment at the region level.

### XHTML/Data Definition

XHTML / Data Definition Blocks can essentially be compared to a Page. However,
these items cannot be published on their own. They have to be assigned to a region
before being rendered to a page.

To use a simple XHTML (WYSIWYG) you simply add a new Block (`Add Content > Default > Block`) to your site
and fill in the Editor content.

To use a Data Definition, click `Properties` and assign the appropriate Data Definition
and/or meta data set.

**Reminder:** Blocks cannot be published independently and this content will only
be rendered to a page IF it is assigned on the Template, Configuration, or Page Level.

### XML

An XML Block is a reusable piece of content stored as well-formed, static XML.
These blocks are useful when there is a large amount of XML that must be styles and
included on one or more pages.

### Feed Block

A feed block pulls in an XML RSS/ATOM feed for use when aggregating content. This can
be useful when aggregating outside RSS links or receiving output from dynamic scripts
or web applications that produce XML.

Feed Blocks are updated every time the block is rendered. Therefore updates happen
within the Cascade interface NOT on the web. These updates can also be triggered
using the FeedBlock API.

### Text

Text blocks are the most basic type of content. Typically a XHTML block will be 
more utilized, but if text formatting is not needed, this is an excellent option.

### Index

Index Blocks are dynamically generated system assets, as XML. They can be used
to aggregate folders, files or assets (or a combination of all).

Index blocks are typically used for creating dynamic content such as navigation menus,
sitemaps, etc.

Index blocks can be used on an individual folder, or across an entire site.

Configuration settings will vary depending on the needs of the site.

## Using Blocks

Blocks can be added using `Add Content > Default > Block`. You then select the type
of block you want and update the corresponding settings.

All Blocks require a Name and Title and can be placed in whatever folder desired.

### XHTML/Data Definition

If using a WYSIWYG, simply enter the necessary information/code.

If using a Data Definition, select `Properties` and the appropriate Data Definition.

### XML

An XML Block requires well-formed XML to be used.

### Text

Fill out the plain text content as desired.

### Index

The index block is the most complicated, as there are a number of settings.

#### Index Block Settings

- Index Type:
  - **Folder:** Renders assets from a specific folder (determined as selected OR based on the current page)
  - *Content Type:* Renders assets that use a specific Content Type. Only *ONE* content type can be used per block
- **Index Folder:** When selected, will render out the assets based on the folder selected. This folder is static to the block
  and will not necessarily be dynamic within a specific site.
- **Rendering Behavior:**
  1. Render Normally, starting at indexed folder -- Will render based off the folder selected
  2. Start at current page and include its folder hierarchy -- Will render based off the *CURRENT PAGE* and include the folder structure
  3. Start at the current page with folder hierarchy, and also include siblings -- Renders from the current page and includes the folder structure and the children of the current folder
  4. Start at the current page with folder hierarchy, siblings and also render forward -- Expands on the above. Is basically a combination of 1 and 3.
- **Depth of Index:** Helps outline the folder depth, or how far you want to render out. If you have nested files/folders place the number you'd want here. It's okay to overshoot! 1 will only render 1 layer deep.
- **Max Rendered Assets:** 0 will render all available assets (meeting the criteria), otherwise you can set a hard cap./
- **Index Asset Content:** This adds "content" to the XML structure for access
  - Append Calling Page Data -- Appends data from the Page, which includes this index block
  - Regular Content -- Content available to users to edit
  - System Metadata -- System information, such as created and last updated date
  - User Metadata -- Includes metadata users can change
  - Tags
  - Folder Access Rights
  - User Information
  - Workflow Information
- **Indexed Asset Types:** Determine what files/assets you want included in the block
 - Pages, Blocks, Links, Files
- **Page XML:** What content (if available) is rendered and within the Block for Pages. Must have Pages as an asset type AND Regular Content selected for this option to be available
- **Block XML:** Similar to above, but for blocks.
- **Sort Method and Order:** Determine how you want items sorted and in which direction.


### Feed

Fill in the feed URL you wish to pull in.