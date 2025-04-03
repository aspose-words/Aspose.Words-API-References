---
title: OutlineOptions.createMissingOutlineLevels property
linktitle: createMissingOutlineLevels property
articleTitle: createMissingOutlineLevels property
second_title: Aspose.Words for NodeJs
description: "OutlineOptions.createMissingOutlineLevels property. Gets or sets a value determining whether or not to create missing outline levels when the document is  exported."
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Saving/outlineoptions/createMissingOutlineLevels/
---

## OutlineOptions.createMissingOutlineLevels property

Gets or sets a value determining whether or not to create missing outline levels when the document is 
exported.

Default value for this property is ``false``.




```js
get createMissingOutlineLevels(): boolean
```

### Examples

Shows how to work with outline levels that do not contain any corresponding headings when saving a PDF document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert headings that can serve as TOC entries of levels 1 and 5.
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading1;

expect(builder.paragraphFormat.isHeading).toEqual(true);

builder.writeln("Heading 1");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading5;

builder.writeln("Heading 1.1.1.1.1");
builder.writeln("Heading 1.1.1.1.2");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let saveOptions = new aw.Saving.PdfSaveOptions();

// The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "5" to include all headings of levels 5 and below in the outline.
saveOptions.outlineOptions.headingsOutlineLevels = 5;

// This document contains headings of levels 1 and 5, and no headings with levels of 2, 3, and 4.
// The output PDF document will treat outline levels 2, 3, and 4 as "missing".
// Set the "CreateMissingOutlineLevels" property to "true" to include all missing levels in the outline,
// leaving blank outline entries since there are no usable headings.
// Set the "CreateMissingOutlineLevels" property to "false" to ignore missing outline levels,
// and treat the outline level 5 headings as level 2.
saveOptions.outlineOptions.createMissingOutlineLevels = createMissingOutlineLevels;

doc.save(base.artifactsDir + "PdfSaveOptions.createMissingOutlineLevels.pdf", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [OutlineOptions](../)

