---
title: Save
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 680
url: /net/aspose.words/document/save/
---
## Save(string) {1}

Saves the document to a file. Automatically determines the save format from the extension.

```csharp
public SaveOutputParameters Save(string fileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |

### Return Value

Additional information that you can optionally use.

### Examples

Shows how to open a document and convert it to .PDF.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

Shows how to convert a PDF to a .docx.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// Load the PDF document that we just saved, and convert it to .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

### See Also

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

---

## Save(string, SaveFormat) {2}

Saves the document to a file in the specified format.

```csharp
public SaveOutputParameters Save(string fileName, SaveFormat saveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |
| saveFormat | SaveFormat | The format in which to save the document. |

### Return Value

Additional information that you can optionally use.

### Examples

Shows how to convert from DOCX to HTML format.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### See Also

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters)
* enum [SaveFormat](../../saveformat)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

---

## Save(string, SaveOptions) {3}

Saves the document to a file using the specified save options.

```csharp
public SaveOutputParameters Save(string fileName, SaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |
| saveOptions | SaveOptions | Specifies the options that control how the document is saved. Can be null. |

### Return Value

Additional information that you can optionally use.

### Examples

Shows how to improve the quality of a rendered document with SaveOptions.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 60;
builder.Writeln("Some text.");

SaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.Default.jpg", options);

options.UseAntiAliasing = true;
options.UseHighQualityRendering = true;

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.HighQuality.jpg", options);
```

Shows how to convert a PDF to a .docx and customize the saving process with a SaveOptions object.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

// Load the PDF document that we just saved, and convert it to .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);

// Set the "Password" property to encrypt the saved document with a password.
saveOptions.Password = "MyPassword";

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.docx", saveOptions);
```

Shows how to render every page of a document to a separate TIFF image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Set the "PageSet" property to the number of the first page from
    // which to start rendering the document from.
    options.PageSet = new PageSet(i);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

Shows how to render one page from a document to a JPEG image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

// Set the "PageSet" to "1" to select the second page via
// the zero-based index to start rendering the document from.
options.PageSet = new PageSet(1);

// When we save the document to the JPEG format, Aspose.Words only renders one page.
// This image will contain one page starting from page two,
// which will just be the second page of the original document.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

Shows how to configure compression while saving a document as a JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Set the "JpegQuality" property to "10" to use stronger compression when rendering the document.
// This will reduce the file size of the document, but the image will display more prominent compression artifacts.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
// This will improve the quality of the image at the cost of an increased file size.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

Shows how to convert a whole document to PDF with three levels in the document outline.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert headings of levels 1 to 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
// an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
// In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
// the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on. 
// In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
// Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
// and collapse all level and 3 and higher entries when we open the document. 
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### See Also

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters)
* class [SaveOptions](../../../aspose.words.saving/saveoptions)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

---

## Save(Stream, SaveFormat) {4}

Saves the document to a stream using the specified format.

```csharp
public SaveOutputParameters Save(Stream stream, SaveFormat saveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | Stream where to save the document. |
| saveFormat | SaveFormat | The format in which to save the document. |

### Return Value

Additional information that you can optionally use.

### Examples

Shows how to save a document to a stream.

```csharp
Document doc = new Document(MyDir + "Document.docx");

using (MemoryStream dstStream = new MemoryStream())
{
    doc.Save(dstStream, SaveFormat.Docx);

    // Verify that the stream contains the document.
    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", new Document(dstStream).GetText().Trim());
}
```

Shows how to save a document to an image via stream, and then read the image from that stream.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

#if NET48 || JAVA
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                // Read the stream back into an image.
                using (Image image = Image.FromStream(stream))
                {
                    Assert.AreEqual(ImageFormat.Bmp, image.RawFormat);
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#elif NET5_0 || __MOBILE__
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                SKCodec codec = SKCodec.Create(stream);

                Assert.AreEqual(SKEncodedImageFormat.Bmp, codec.EncodedFormat);

                stream.Position = 0;

                using (SKBitmap image = SKBitmap.Decode(stream))
                {
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#endif
```

### See Also

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters)
* enum [SaveFormat](../../saveformat)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

---

## Save(Stream, SaveOptions) {5}

Saves the document to a stream using the specified save options.

```csharp
public SaveOutputParameters Save(Stream stream, SaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | Stream where to save the document. |
| saveOptions | SaveOptions | Specifies the options that control how the document is saved. Can be null. If this is null, the document will be saved in the binary DOC format. |

### Return Value

Additional information that you can optionally use.

### Examples

Shows how to convert only some of the pages in a document to PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
    // to modify how that method converts the document to .PDF.
    PdfSaveOptions options = new PdfSaveOptions();

    // Set the "PageIndex" to "1" to render a portion of the document starting from the second page.
    options.PageSet = new PageSet(1);

    // This document will contain one page starting from page two, which will only contain the second page.
    doc.Save(stream, options);
}
```

### See Also

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters)
* class [SaveOptions](../../../aspose.words.saving/saveoptions)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

---

## Save(HttpResponse, string, ContentDisposition, SaveOptions) {6}

Sends the document to the client browser.

```csharp
public SaveOutputParameters Save(HttpResponse response, string fileName, 
    ContentDisposition contentDisposition, SaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| response | HttpResponse | Response object where to save the document. |
| fileName | String | The name for the document that will appear at the client browser. The name should not contain path. |
| contentDisposition | ContentDisposition | A [`ContentDisposition`](../../contentdisposition) value that specifies how the document is presented at the client browser. |
| saveOptions | SaveOptions | Specifies the options that control how the document is saved. Can be null. |

### Return Value

Additional information that you can optionally use.

### Remarks

Internally, this method saves to a memory stream first and then copies to the response stream because the response stream does not support seek.

### Examples

Shows how to perform a mail merge, and then save the document to the client browser.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Send the document to the client browser.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //Thrown because HttpResponse is null in the test.

// We will need to close this response manually to ensure that we do not add any superfluous content to the document after saving.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### See Also

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters)
* enum [ContentDisposition](../../contentdisposition)
* class [SaveOptions](../../../aspose.words.saving/saveoptions)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
