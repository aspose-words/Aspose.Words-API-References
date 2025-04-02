---
title: PageSetup.paperSize property
linktitle: paperSize property
articleTitle: paperSize property
second_title: Aspose.Words for NodeJs
description: "PageSetup.paperSize property. Returns or sets the paper size."
type: docs
weight: 350
url: /nodejs-net/Aspose.Words/pagesetup/paperSize/
---

## PageSetup.paperSize property

Returns or sets the paper size.


```js
get paperSize(): Aspose.Words.PaperSize
```

### Remarks

Setting this property updates [PageSetup.pageWidth](../pageWidth/) and [PageSetup.pageHeight](../pageHeight/) values.
Setting this value to [PaperSize.Custom](../../papersize/#Custom) does not change existing values.




### Examples

Shows how to adjust paper size, orientation, margins, along with other settings for a section.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.pageSetup.paperSize = aw.PaperSize.Legal;
builder.pageSetup.orientation = aw.Orientation.Landscape;
builder.pageSetup.topMargin = aw.ConvertUtil.inchToPoint(1.0);
builder.pageSetup.bottomMargin = aw.ConvertUtil.inchToPoint(1.0);
builder.pageSetup.leftMargin = aw.ConvertUtil.inchToPoint(1.5);
builder.pageSetup.rightMargin = aw.ConvertUtil.inchToPoint(1.5);
builder.pageSetup.headerDistance = aw.ConvertUtil.inchToPoint(0.2);
builder.pageSetup.footerDistance = aw.ConvertUtil.inchToPoint(0.2);

builder.writeln("Hello world!");

doc.save(base.artifactsDir + "PageSetup.pageMargins.docx");
```

Shows how to set page sizes.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// We can change the current page's size to a pre-defined size
// by using the "PaperSize" property of this section's PageSetup object.
builder.pageSetup.paperSize = aw.PaperSize.Tabloid;

expect(builder.pageSetup.pageWidth).toEqual(792.0);
expect(builder.pageSetup.pageHeight).toEqual(1224.0);

builder.writeln(`This page is ${builder.pageSetup.pageWidth}x${builder.pageSetup.pageHeight}.`);

// Each section has its own PageSetup object. When we use a document builder to make a new section,
// that section's PageSetup object inherits all the previous section's PageSetup object's values.
builder.insertBreak(aw.BreakType.SectionBreakEvenPage);

expect(builder.pageSetup.paperSize).toEqual(aw.PaperSize.Tabloid);

builder.pageSetup.paperSize = aw.PaperSize.A5;
builder.writeln(`This page is ${builder.pageSetup.pageWidth}x${builder.pageSetup.pageHeight}.`);

expect(builder.pageSetup.pageWidth).toEqual(419.55);
expect(builder.pageSetup.pageHeight).toEqual(595.30);

builder.insertBreak(aw.BreakType.SectionBreakEvenPage);

// Set a custom size for this section's pages.
builder.pageSetup.pageWidth = 620;
builder.pageSetup.pageHeight = 480;

expect(builder.pageSetup.paperSize).toEqual(aw.PaperSize.Custom);

builder.writeln(`This page is ${builder.pageSetup.pageWidth}x${builder.pageSetup.pageHeight}.`);

doc.save(base.artifactsDir + "PageSetup.PaperSizes.docx");
```

Shows how to construct an Aspose.words document by hand.

```js
let doc = new aw.Document();

// A blank document contains one section, one body and one paragraph.
// Call the "RemoveAllChildren" method to remove all those nodes,
// and end up with a document node with no children.
doc.removeAllChildren();

// This document now has no composite child nodes that we can add content to.
// If we wish to edit it, we will need to repopulate its node collection.
// First, create a new section, and then append it as a child to the root document node.
let section = new aw.Section(doc);
doc.appendChild(section);

// Set some page setup properties for the section.
section.pageSetup.sectionStart = aw.SectionStart.NewPage;
section.pageSetup.paperSize = aw.PaperSize.Letter;

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
let body = new aw.Body(doc);
section.appendChild(body);

// Create a paragraph, set some formatting properties, and then append it as a child to the body.
let para = new aw.Paragraph(doc);

para.paragraphFormat.styleName = "Heading 1";
para.paragraphFormat.alignment = aw.ParagraphAlignment.Center;

body.appendChild(para);

// Finally, add some content to do the document. Create a run,
// set its appearance and contents, and then append it as a child to the paragraph.
let run = new aw.Run(doc);
run.text = "Hello World!";
run.font.color = "#FF0000";
para.appendChild(run);

expect(doc.getText().trim()).toEqual("Hello World!");

doc.save(base.artifactsDir + "Section.CreateManually.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)

