---
title: 'Formats'
date: 2018-11-28T15:14:39+10:00
weight: 4
bookFlatSection: false
bookToc: true
---

# Formats

## Overview

Cascade content is stored as XML data. In order to display that properly,
we use formats to transform the content into useful markup.

At Xavier we have determined Velocity (Apache's Velocity Templating Language) to be 
our language of choice for creating formats. XSLT is also available for use.

Both types of Formats can be assigned to regions but cannot be combined into a singular region.

## Uses for Foats

Formats can be applied along with [Blocks](blocks) to a specific region in a page.
Applying both the block and the format together ensures that the foramt