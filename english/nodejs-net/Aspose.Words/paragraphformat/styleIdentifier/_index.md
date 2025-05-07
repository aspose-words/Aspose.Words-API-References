---
title: ParagraphFormat.styleIdentifier property
linktitle: styleIdentifier property
articleTitle: styleIdentifier property
second_title: Aspose.Words for Node.js
description: "ParagraphFormat.styleIdentifier property. Gets or sets the locale independent style identifier of the paragraph style applied to this formatting."
type: docs
weight: 360
url: /nodejs-net/aspose.words/paragraphformat/styleIdentifier/
---

## ParagraphFormat.styleIdentifier property

Gets or sets the locale independent style identifier of the paragraph style applied to this formatting.


```js
get styleIdentifier(): Aspose.Words.StyleIdentifier
```

### Examples

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a table of contents for the first page of the document.
// Configure the table to pick up paragraphs with headings of levels 1 to 3.
// Also, set its entries to be hyperlinks that will take us
// to the location of the heading when left-clicked in Microsoft Word.
builder.insertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.insertBreak(aw.BreakType.PageBreak);

// Populate the table of contents by adding paragraphs with heading styles.
// Each such heading with a level between 1 and 3 will create an entry in the table.
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading1;
builder.writeln("Heading 1");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading2;
builder.writeln("Heading 1.1");
builder.writeln("Heading 1.2");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading1;
builder.writeln("Heading 2");
builder.writeln("Heading 3");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading2;
builder.writeln("Heading 3.1");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading3;
builder.writeln("Heading 3.1.1");
builder.writeln("Heading 3.1.2");
builder.writeln("Heading 3.1.3");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading4;
builder.writeln("Heading 3.1.3.1");
builder.writeln("Heading 3.1.3.2");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading2;
builder.writeln("Heading 3.2");
builder.writeln("Heading 3.3");

// A table of contents is a field of a type that needs to be updated to show an up-to-date result.
doc.updateFields();
doc.save(base.artifactsDir + "DocumentBuilder.InsertToc.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

