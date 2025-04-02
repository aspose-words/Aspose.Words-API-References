---
title: PageSetup.oddAndEvenPagesHeaderFooter property
linktitle: oddAndEvenPagesHeaderFooter property
articleTitle: oddAndEvenPagesHeaderFooter property
second_title: Aspose.Words for NodeJs
description: "PageSetup.oddAndEvenPagesHeaderFooter property. True if the document has different headers and footers for odd-numbered and even-numbered pages."
type: docs
weight: 280
url: /nodejs-net/Aspose.Words/pagesetup/oddAndEvenPagesHeaderFooter/
---

## PageSetup.oddAndEvenPagesHeaderFooter property

True if the document has different headers and footers for odd-numbered and even-numbered pages.


```js
get oddAndEvenPagesHeaderFooter(): boolean
```

### Remarks

Note, changing this property affects all sections in the document.


### Examples

Shows how to enable or disable even page headers/footers.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Below are two types of header/footers.
// 1 -  The "Primary" header/footer, which appears on every page in the section.
// We can override the primary header/footer by a first and an even page header/footer. 
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);
builder.writeln("Primary header.");

builder.moveToHeaderFooter(aw.HeaderFooterType.FooterPrimary);
builder.writeln("Primary footer.");

// 2 -  The "Even" header/footer, which appears on every even page of this section.
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderEven);
builder.writeln("Even page header.");

builder.moveToHeaderFooter(aw.HeaderFooterType.FooterEven);
builder.writeln("Even page footer.");

builder.moveToSection(0);
builder.writeln("Page 1.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 2.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 3.");

// Each section has a "PageSetup" object that specifies page appearance-related properties
// such as orientation, size, and borders.
// Set the "OddAndEvenPagesHeaderFooter" property to "true"
// to display the even page header/footer on even pages.
// Set the "OddAndEvenPagesHeaderFooter" property to "false"
// to display the primary header/footer on even pages.
builder.pageSetup.oddAndEvenPagesHeaderFooter = oddAndEvenPagesHeaderFooter;

doc.save(base.artifactsDir + "PageSetup.oddAndEvenPagesHeaderFooter.docx");
```

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

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)

