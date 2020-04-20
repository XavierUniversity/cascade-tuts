---
title: 'Data Definition'
date: 2020-04-15t16:22:00
weight: 4
summary: Datadefinitions define the user editable features of an asset.
---

# What are Data Definitions?

Data Definitions are the editable features of a specific page or block.

## Xavier Example

Continuing on our Content Page example, the Data Definition is defined to include:

1. Hero (Group)
    - 
2. WYSIWYG (wysiwyg editor)
    - Uses a custom WYSIWYG Configuration to hide/show various features, which gives 
    dev staff additional control over what the users are able to insert onto their pages.
3. Extras (Group)
    - Custom files (JS and CSS) which is available to administrative groups only

What you cannot see from the page editor itself, is that all of these items are
considered "[Shared Fields](#shared-fields)". These fields are reusable elements that allow for minimal
management, but widespread use across multiple data definitions.

## Shared Fields

Shared fields are individual fields (e.g. WYSIWYG editor) or individual groups of fields (e.g. Hero). These
fields allow us to create reusable entities for multiple data definitions. A big example of this is the extra's group.

### Extras Shared Field

The Extra's group is used on all data definitions to be able to add custom stylesheets and/or scripts
to either add or supplement functionality on an individual page. Rather than code this individually
to each Data Definition, the shared field was created to be able to reuse, rather than duplicate.

## Smart Fields

Smart fields are used to show or hide subsequent sections based on a user selection. 

### Example

- User selects `internal` on a radio button, showing a page chooser
- Alternatively, user selects `external` and receives a text box

## Creating a Data Definition

To create a Data Definition

1. Navigate to Manage Site > Data Definitions. You may also want to add a new 
container, depending on the architecture desired.
2. Enter the Name and select the Parent Container, as desired.
3. Using either the Builder or XML editor, add or update your desired fields.
    - We recommend using the Builder to setup the initial data definition, and review the XML for a better understanding.
    - Shared Fields can be used by adding a field and selecting Choose Shared Field
    - Smart fields can be used by viewing the Advanced Options

{{< hint warning >}}    
**Data Definition Warning**

Restructuring and/or renaming of fields may cause a loss of content. Use caution when 
moving a field out of a group and/or into a group that doesn't permit multiple groups 
OR has a lower maximum number of groups allowed.
{{< /hint >}}