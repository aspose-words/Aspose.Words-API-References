---
title: DocumentBuilder.moveToHeaderFooter method
linktitle: moveToHeaderFooter method
articleTitle: moveToHeaderFooter method
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.moveToHeaderFooter method. Moves the cursor to the beginning of a header or footer in the current section."
type: docs
weight: 580
url: /nodejs-net/Aspose.Words/documentbuilder/moveToHeaderFooter/
---

## moveToHeaderFooter(headerFooterType) {#headerfootertype}

Moves the cursor to the beginning of a header or footer in the current section.


```js
moveToHeaderFooter(headerFooterType: Aspose.Words.HeaderFooterType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | [HeaderFooterType](../../headerfootertype/) | Specifies the header or footer to move to. |

### Remarks

After you moved the cursor into a header or footer, you can use the rest of [DocumentBuilder](../)
methods to modify the contents of the header or footer.

If you want to create headers and footers different for the first page, you need
to set [PageSetup.differentFirstPageHeaderFooter](../../pagesetup/differentFirstPageHeaderFooter/).

If you want to create headers and footers different for even and odd pages, you need
to set [PageSetup.oddAndEvenPagesHeaderFooter](../../pagesetup/oddAndEvenPagesHeaderFooter/).

Use [DocumentBuilder.moveToSection()](../moveToSection/#number) to move out of the header into the main text.




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

Shows how to insert an image, and use it as a watermark.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert the image into the header so that it will be visible on every page.
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);
let shape = builder.insertImage(base.imageDir + "Transparent background logo.png");
shape.wrapType = aw.Drawing.WrapType.None;
shape.behindText = true;

// Place the image at the center of the page.
shape.relativeHorizontalPosition = aw.Drawing.RelativeHorizontalPosition.Page;
shape.relativeVerticalPosition = aw.Drawing.RelativeVerticalPosition.Page;
shape.left = (builder.pageSetup.pageWidth - shape.width) / 2;
shape.top = (builder.pageSetup.pageHeight - shape.height) / 2;

doc.save(base.artifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

