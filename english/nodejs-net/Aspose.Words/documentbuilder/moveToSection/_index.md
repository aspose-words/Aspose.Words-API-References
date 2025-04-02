---
title: DocumentBuilder.moveToSection method
linktitle: moveToSection method
articleTitle: moveToSection method
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.moveToSection method. Moves the cursor to the beginning of the body in a specified section."
type: docs
weight: 610
url: /nodejs-net/Aspose.Words/documentbuilder/moveToSection/
---

## moveToSection(sectionIndex) {#number}

Moves the cursor to the beginning of the body in a specified section.


```js
moveToSection(sectionIndex: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| sectionIndex | number | The index of the section to move to. |

### Remarks

When *sectionIndex* is greater than or equal to 0, it specifies an index from
the beginning of the document with 0 being the first section. When*sectionIndex* is less than 0,
it specified an index from the end of the document with -1 being the last section.

The cursor is moved to the first paragraph in the [Body](../../body/) of the specified section.




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

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

