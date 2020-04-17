---
title: 'Configurations'
date: 2020-04-15T19:27:37+10:00
weight: 2
---

# What are Configurations?

Configurations are collections of one or more outputs used to display page content. 
Outputs allow the same content to take different forms (PDF, JSON, HTML, etc).

Here at Xavier we create new configurations for the various Content Types. In V5,
we are using the Configurations to reroute code to the proper formats based on the Content Type (e.g. Content, Landing Page, Academic Page, etc.).

A more detailed definition can be found on the Cascade CMS Knowledge Base for [Configurations](https://www.hannonhill.com/cascadecms/latest/design-in-cascade/configurations/index.html#Overview).

## Xavier Example:

For content pages, we have 7 different configurations. The most basic is the Content Configuration where we 
swap the `DEFAULT` region with the appropriate Content Page format to ensure we write out the proper
code foundation.

**Configuration Settings**

- **Name:** PHP
- **Type of Data:** HTML
- **File Extension:** PHP
- **Template:** v5
- **XSLT Format:** none
- **Template Defined Regions:**
  - Custom JS, Footer, Head Content, Header, SVG
- **Configuration Defined Regions:**
  - DEFAULT - Inside of the custom format, we build out the content page structure
    - In most configurations, this is the ONLY item that will change.

## Creating a Configuration

1. Navigate to Manage Site > Configurations
2. Add a new Configuration using Add > Configuration. You may also want to add a new
container, depending on the architecture desired.
3. Enter the Name and select the Parent Container, as desired.
4. In the next section, you'll define the outputs, each output is configured using the following fields:
  - Name (req)
  - Default Output
  - Type of Data - This only affects how the data is viewed within Cascade
  - File Extension (req) - e.g. php, html. This will be appended to the file when published
  - Template
  - XSLT Format
  - Publishable - Helpful to prevent pages you may want to keep on Cascade vs being published to the server
  - Include XML Declaration in Published Files
  - Regions
    - This will override any TEMPLATE level assignments
5. Preview & Submit!

You can [link to specific outputs](https://www.hannonhill.com/cascadecms/latest/design-in-cascade/configurations/linking-to-specific-outputs.html) if desired, but this is not a feature we are currently using at Xavier.

