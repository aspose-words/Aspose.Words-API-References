---
title: Document.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Document.save method"
type: docs
weight: 700
url: /nodejs-net/Aspose.Words/document/save/
---

## save(stream, saveFormat) {#unknown_saveformat}

```js
save(streamsaveFormat: Aspose.Words.SaveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream |  |  |
| saveFormat | [SaveFormat](../../saveformat/) |  |

## save(stream, saveOptions) {#unknown_saveoptions}

```js
save(streamsaveOptions: Aspose.Words.Saving.SaveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream |  |  |
| saveOptions | [SaveOptions](../../../aspose.words.saving/saveoptions/) |  |

## save(fileName) {#string}

Saves the document to a file. Automatically determines the save format from the extension.


```js
save(fileName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |

### Returns

Additional information that you can optionally use.


## save(fileName, saveFormat) {#string_saveformat}

Saves the document to a file in the specified format.


```js
save(fileName: stringsaveFormat: Aspose.Words.SaveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |
| saveFormat | [SaveFormat](../../saveformat/) | The format in which to save the document. |

### Returns

Additional information that you can optionally use.


## save(fileName, saveOptions) {#string_saveoptions}

Saves the document to a file using the specified save options.


```js
save(fileName: stringsaveOptions: Aspose.Words.Saving.SaveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |
| saveOptions | [SaveOptions](../../../aspose.words.saving/saveoptions/) | Specifies the options that control how the document is saved. Can be ``None``. |

### Returns

Additional information that you can optionally use.


## Examples

Shows how to open a document and convert it to .PDF.

```js
const doc = new aw.Document(base.myDir + "Document.docx");
doc.save(base.artifactsDir + "Document.ConvertToPdf.pdf");
```

Shows how to convert a PDF to a .docx.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Hello world!");

doc.save(base.artifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// Load the PDF document that we just saved, and convert it to .docx.
let pdfDoc = new aw.Document(base.artifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.save(base.artifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

Shows how to convert from DOCX to HTML format.

```js
const doc = new aw.Document(base.myDir + "Document.docx");

doc.save(base.artifactsDir + "Document.ConvertToHtml.html", aw.SaveFormat.Html);
```

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

Shows how to configure compression while saving a document as a JPEG.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.insertImage(base.imageDir + "Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
let imageOptions = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Jpeg);
// Set the "JpegQuality" property to "10" to use stronger compression when rendering the document.
// This will reduce the file size of the document, but the image will display more prominent compression artifacts.
imageOptions.jpegQuality = 10;
doc.save(base.artifactsDir + "ImageSaveOptions.jpegQuality.HighCompression.jpg", imageOptions);

// Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
// This will improve the quality of the image at the cost of an increased file size.
imageOptions.jpegQuality = 100;
doc.save(base.artifactsDir + "ImageSaveOptions.jpegQuality.HighQuality.jpg", imageOptions);
```

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

Shows how to convert a PDF to a .docx and customize the saving process with a SaveOptions object.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Hello world!");

doc.save(base.artifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

// Load the PDF document that we just saved, and convert it to .docx.
let pdfDoc = new aw.Document(base.artifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

let saveOptions = new aw.Saving.OoxmlSaveOptions(aw.SaveFormat.Docx);

// Set the "Password" property to encrypt the saved document with a password.
saveOptions.password = "MyPassword";

pdfDoc.save(base.artifactsDir + "PDF2Word.ConvertPdfToDocxCustom.docx", saveOptions);
```

## See Also

* module [Aspose.Words](../../)
* class [Document](../)

