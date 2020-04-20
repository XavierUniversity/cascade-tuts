---
title: 'Content Types'
date: 2020-04-15T19:27:37+10:00
weight: 3
summary: Content Types combine the look and feel to the editable fields.
---

# What are Content Types?

Content types combine the look and feel ([Configuration](configurations)) to editable content fields ([Metadata Set](metadata) and [Data Definition](data-definition)) so non-technical users can create and edit pages.

In order to create a Content Type you must first setup a [Configuration](configurations), [Metadata Set](metadata), and determine if you want to use a WYSIWYG or a [Data Definition](data-definition). These items _can_ be modified after they are linked to a Content Type.

## Xavier Example:

Staying with our Content Page example, we tie the Content Page DD, our default Metadata Set and Content Configuration 
to be able to output the proper content.

**Content Type Settings**

- **Name:** V5 Content Page Content Type
- **Configuration:** Content Configuration
- **Metadata Set:** Default
- **Type of Content:** Data Definition
- **Data Definition:** Content Page

## Creating a Content Type

1. Navigate to Manage Site > Content Types
2. Add a new Configuration using Add > Content Type. You may also want to add a new
container, depending on the architecture desired.
3. Enter the Name and select the Parent Container, as desired.
4. In the Settings Tab, select the following
  - Configuration
  - Metadata Set
  - Type of Content - Either Data Definition or WYSIWYG
    - Data Definitions need to be defined before this can be used.
    - The WYSIWYG option will put in a basic WYISWYG item with no additional fields
5. Submit.

Additional options are available but are not used by Xavier at this time and information on those can be found on the Cascade CMS [Content Type](https://www.hannonhill.com/cascadecms/latest/design-in-cascade/content-types/index.html) Knowledge Base article.