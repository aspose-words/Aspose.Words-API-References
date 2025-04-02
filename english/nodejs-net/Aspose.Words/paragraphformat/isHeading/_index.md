---
title: ParagraphFormat.isHeading property
linktitle: isHeading property
articleTitle: isHeading property
second_title: Aspose.Words for NodeJs
description: "ParagraphFormat.isHeading property. True when the paragraph style is one of the built-in Heading styles."
type: docs
weight: 140
url: /nodejs-net/Aspose.Words/paragraphformat/isHeading/
---

## ParagraphFormat.isHeading property

True when the paragraph style is one of the built-in Heading styles.


```js
get isHeading(): boolean
```

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

### See Also

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

