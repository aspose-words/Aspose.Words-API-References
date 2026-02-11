---
title: HeaderFooterType enumeration
linktitle: HeaderFooterType enumeration
articleTitle: HeaderFooterType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.HeaderFooterType enumeration. Identifies the type of header or footer found in a Word file."
type: docs
weight: 520
url: /nodejs-net/aspose.words/headerfootertype/
---

## HeaderFooterType enumeration

Identifies the type of header or footer found in a Word file.


### Members

| Name | Description |
| --- | --- |
| HeaderEven | Header for even numbered pages. |
| HeaderPrimary | Primary header, also used for odd numbered pages. |
| FooterEven | Footer for even numbered pages. |
| FooterPrimary | Primary footer, also used for odd numbered pages. |
| HeaderFirst | Header for the first page of the section. |
| FooterFirst | Footer for the first page of the section. |

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

### See Also

* module [Aspose.Words](../)

