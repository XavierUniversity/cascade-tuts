---
title: 'Code Sections'
date: 2018-11-28T15:14:39+10:00
weight: 3
bookFlatSection: false
bookToc: true
---

# Code Sections

Code sections allow for code, that may not necessarily be valid code in the eyes
of Cascade. 

In our environment, we have noticed PHP, JS and SVG being the largest culprits.

## Passthrough Code Sections

Passthrough code sections instruct the interpreter to exclude the enclosed code
when the page is being previewed internally. Upon publishing, the contents of these
tags will be uncommented and included in the final page.

```html
<!--#passthrough ...put any code here... #passthrough-->
```

When viewing a file or page containing these types of blocks within the CMS,
these sections are left untouched unless the asset is a page with serialization type
of PDF or RTF. In this case, these sections are removed.

## Passthrough-Top Code Sections

Passthrough-Top is used to support code that must be placed at the very top of a document.
The rules for rendering are the same as above.

```html
<!--#passthrough-top ...put any code here... #passthrough-top-->
```

Multiple sections of passthrough-top would be placed sequentially at the top of the document
in relative order they appeared.

## Protect Code Sections

These code sections work the same as passthrough code sections with the exception
that protect code sections are also rendered inside of Cascade CMS. Because
of that, the purpose of these code sections is shifted from outputting server side
code to client side code such as Javascript. This also allows outputting
unbalanced XML for old browser support.

```html
<!--#protect ...put any code here... #protect-->
```

or

```html
<![CDATA[#protect ...put any code here... #protect]]>
```

Using the CDATA format allows for special sequences of characters to be entered such
as `--` which is commonly used in Javascript as a decrement operation.

## Protect-Top Code Sections

These code sections work just as passthrough-top code sections but again with the
exception that protect-top code sections are also rendered inside of Cascade CMS.
You can use these to output a non-standard doctype, or use Cascade CMS to dynamically render non XML content.

```html
<!--#protect-top ...put any code here... #protect-top-->
```

or

```html
<![CDATA[#protect-top ...put any code here... #protect-top]]>
```

## Cascade Skip Tags

In some situations it is useful to completely remove part of the code. This is possible
through outputting `#cacsade-skip` tag inside of html comments. For example:

```xml
<xml><!--#cascade-skip--><unnecessary-tag/><!--#cascade-skip-->
```

Placing only one `<!--#cascade-skip-->` tag results with the remaining contents being fully stripped.
This is useful together with the `#protect-top` tag.