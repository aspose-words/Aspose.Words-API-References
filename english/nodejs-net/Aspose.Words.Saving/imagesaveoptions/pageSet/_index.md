---
title: ImageSaveOptions.pageSet property
linktitle: pageSet property
articleTitle: pageSet property
second_title: Aspose.Words for Node.js
description: "ImageSaveOptions.pageSet property. Gets or sets the pages to render"
type: docs
weight: 100
url: /nodejs-net/aspose.words.saving/imagesaveoptions/pageSet/
---

## ImageSaveOptions.pageSet property

Gets or sets the pages to render.
Default is all the pages in the document.


```js
get pageSet(): Aspose.Words.Saving.PageSet
```

### Remarks

This property has effect only when rendering document pages. This property is ignored when rendering shapes to images.




### Examples

Shows how to render one page from a document to a JPEG image.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Page 1.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 2.");
builder.insertImage(base.imageDir + "Logo.jpg");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 3.");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
let options = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Jpeg);
// Set the "PageSet" to "1" to select the second page via
// the zero-based index to start rendering the document from.
options.pageSet = new aw.Saving.PageSet(1);

// When we save the document to the JPEG format, Aspose.words only renders one page.
// This image will contain one page starting from page two,
// which will just be the second page of the original document.
doc.save(base.artifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

Shows how to specify which page in a document to render as an image.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.paragraphFormat.style = doc.styles.at("Heading 1");
builder.writeln("Hello world! This is page 1.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("This is page 2.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("This is page 3.");

expect(doc.pageCount).toEqual(3);

// When we save the document as an image, Aspose.words only renders the first page by default.
// We can pass a SaveOptions object to specify a different page to render.
let saveOptions = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Gif);
// Render every page of the document to a separate image file.
for (let i = 1; i <= doc.pageCount; i++)
{
  saveOptions.pageSet = new aw.Saving.PageSet(1);

  doc.save(base.artifactsDir + `ImageSaveOptions.pageIndex.page ${i}.gif`, saveOptions);
}
```

Shows how to render every page of a document to a separate TIFF image.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Page 1.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 2.");
builder.insertImage(base.imageDir + "Logo.jpg");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 3.");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
let options = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Tiff);

for (let i = 0; i < doc.pageCount; i++)
{
  // Set the "PageSet" property to the number of the first page from
  // which to start rendering the document from.
  options.pageSet = new aw.Saving.PageSet(i);
  // Export page at 2325x5325 pixels and 600 dpi.
  options.resolution = 600;
  options.imageSize2 = new aw.JSSize(2325, 5325);

  doc.save(base.artifactsDir + `ImageSaveOptions.PageByPage.${i + 1}.tiff`, options);
}
```

Shows how to extract pages based on exact page ranges.

```js
let doc = new aw.Document(base.myDir + "Images.docx");

let imageOptions = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Tiff);
let pageSet = new aw.Saving.PageSet(new aw.Saving.PageRange(1, 1), new aw.Saving.PageRange(2, 3), new aw.Saving.PageRange(1, 3),
  new aw.Saving.PageRange(2, 4), new aw.Saving.PageRange(1, 1));

imageOptions.pageSet = pageSet;
doc.save(base.artifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [ImageSaveOptions](../)

