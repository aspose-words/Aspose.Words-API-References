---
title: DocumentBuilder.insertBreak method
linktitle: insertBreak method
articleTitle: insertBreak method
second_title: Aspose.Words for Node.js
description: "DocumentBuilder.insertBreak method. Inserts a break of the specified type into the document."
type: docs
weight: 260
url: /nodejs-net/aspose.words/documentbuilder/insertBreak/
---

## insertBreak(breakType) {#breaktype}

Inserts a break of the specified type into the document.


```js
insertBreak(breakType: Aspose.Words.BreakType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| breakType | [BreakType](../../breaktype/) | Specifies the type of the break to insert. |

### Remarks

Use this method to insert paragraph, page, column, section or line break into the document.


### Examples

Shows how to create headers and footers in a document using DocumentBuilder.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Specify that we want different headers and footers for first, even and odd pages.
builder.pageSetup.differentFirstPageHeaderFooter = true;
builder.pageSetup.oddAndEvenPagesHeaderFooter = true;

// Create the headers, then add three pages to the document to display each header type.
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderFirst);
builder.write("Header for the first page");
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderEven);
builder.write("Header for even pages");
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);
builder.write("Header for all other pages");

builder.moveToSection(0);
builder.writeln("Page1");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page2");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page3");

doc.save(base.artifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

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

Shows how to apply and revert page setup settings to sections in a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Modify the page setup properties for the builder's current section and add text.
builder.pageSetup.orientation = aw.Orientation.Landscape;
builder.pageSetup.verticalAlignment = aw.PageVerticalAlignment.Center;
builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

// If we start a new section using a document builder,
// it will inherit the builder's current page setup properties.
builder.insertBreak(aw.BreakType.SectionBreakNewPage);

expect(doc.sections.at(1).pageSetup.orientation).toEqual(aw.Orientation.Landscape);
expect(doc.sections.at(1).pageSetup.verticalAlignment).toEqual(aw.PageVerticalAlignment.Center);

// We can revert its page setup properties to their default values using the "ClearFormatting" method.
builder.pageSetup.clearFormatting();

expect(doc.sections.at(1).pageSetup.orientation).toEqual(aw.Orientation.Portrait);
expect(doc.sections.at(1).pageSetup.verticalAlignment).toEqual(aw.PageVerticalAlignment.Top);

builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.save(base.artifactsDir + "PageSetup.clearFormatting.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

