---
title: PdfSaveOptions.outlineOptions property
linktitle: outlineOptions property
articleTitle: outlineOptions property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.outlineOptions property. Allows to specify outline options."
type: docs
weight: 240
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/outlineOptions/
---

## PdfSaveOptions.outlineOptions property

Allows to specify outline options.


```js
get outlineOptions(): Aspose.Words.Saving.OutlineOptions
```

### Remarks

Outlines can be created from headings and bookmarks.

For headings outline level is determined by the heading level.

It is possible to set the max heading level to be included into outlines or disable heading outlines at all.

For bookmarks outline level may be set in options as a default value for all bookmarks or as individual values for particular bookmarks.

Also, outlines can be exported to XPS format by using the same [PdfSaveOptions.outlineOptions](./) class.




### Examples

Shows how to limit the headings' level that will appear in the outline of a saved PDF document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert headings that can serve as TOC entries of levels 1, 2, and then 3.
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading1;

expect(builder.paragraphFormat.isHeading).toEqual(true);

builder.writeln("Heading 1");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading2;

builder.writeln("Heading 1.1");
builder.writeln("Heading 1.2");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading3;

builder.writeln("Heading 1.2.1");
builder.writeln("Heading 1.2.2");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let saveOptions = new aw.Saving.PdfSaveOptions();
saveOptions.saveFormat = aw.SaveFormat.Pdf;

// The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "2" to exclude all headings whose levels are above 2 from the outline.
// The last two headings we have inserted above will not appear.
saveOptions.outlineOptions.headingsOutlineLevels = 2;

doc.save(base.artifactsDir + "PdfSaveOptions.headingsOutlineLevels.pdf", saveOptions);
```

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
* class [PdfSaveOptions](../)

