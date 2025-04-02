---
title: OutlineOptions.headingsOutlineLevels property
linktitle: headingsOutlineLevels property
articleTitle: headingsOutlineLevels property
second_title: Aspose.Words for NodeJs
description: "OutlineOptions.headingsOutlineLevels property. Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the  document outline."
type: docs
weight: 70
url: /nodejs-net/Aspose.Words.Saving/outlineoptions/headingsOutlineLevels/
---

## OutlineOptions.headingsOutlineLevels property

Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the 
document outline.


```js
get headingsOutlineLevels(): number
```

### Remarks

Specify 0 for no headings in the outline; specify 1 for one level of headings in the outline and so on.

Default is 0. Valid range is 0 to 9.




### Examples

Shows how to convert a whole document to PDF with three levels in the document outline.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert headings of levels 1 to 5.
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading1;

expect(builder.paragraphFormat.isHeading).toEqual(true);

builder.writeln("Heading 1");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading2;

builder.writeln("Heading 1.1");
builder.writeln("Heading 1.2");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading3;

builder.writeln("Heading 1.2.1");
builder.writeln("Heading 1.2.2");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading4;

builder.writeln("Heading 1.2.2.1");
builder.writeln("Heading 1.2.2.2");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading5;

builder.writeln("Heading 1.2.2.2.1");
builder.writeln("Heading 1.2.2.2.2");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
options.outlineOptions.headingsOutlineLevels = 4;

// If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
// an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
// In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
// the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
// In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
// Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
// and collapse all level and 3 and higher entries when we open the document.
options.outlineOptions.expandedOutlineLevels = 2;

doc.save(base.artifactsDir + "PdfSaveOptions.expandedOutlineLevels.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [OutlineOptions](../)

