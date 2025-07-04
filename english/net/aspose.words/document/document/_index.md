---
title: Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words for .NET
description: Effortlessly create blank Word documents with our user-friendly document constructor. Streamline your writing process today!
type: docs
weight: 10
url: /net/aspose.words/document/document/
---
## Document() {#constructor}

Creates a blank Word document.

```csharp
public Document()
```

## Remarks

A blank document is retrieved from resources, and by default, the resulting document looks more like created by Word2007. This blank document contains a default fonts table, minimal default styles, and latent styles.

[`OptimizeFor`](../../../aspose.words.settings/compatibilityoptions/optimizefor/) method can be used to optimize the document contents as well as default Aspose.Words behavior to a particular version of MS Word.

The document paper size is Letter by default. If you want to change page setup, use [`PageSetup`](../../section/pagesetup/).

After creation, you can use [`DocumentBuilder`](../../documentbuilder/) to add document content easily.

## Examples

Shows how to format a run of text using its font property.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Shows how to create simple document.

```csharp
Document doc = new Document();

// New Document objects by default come with the minimal set of nodes
// required to begin adding content such as text and shapes: a Section, a Body, and a Paragraph.
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

Shows how to create and load documents.

```csharp
// There are two ways of creating a Document object using Aspose.Words.
// 1 -  Create a blank document:
Document doc = new Document();

// New Document objects by default come with the minimal set of nodes
// required to begin adding content such as text and shapes: a Section, a Body, and a Paragraph.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 -  Load a document that exists in the local file system:
doc = new Document(MyDir + "Document.docx");

// Loaded documents will have contents that we can access and edit.
Assert.That(doc.FirstSection.Body.FirstParagraph.GetText().Trim(), Is.EqualTo("Hello World!"));

// Some operations that need to occur during loading, such as using a password to decrypt a document,
// can be done by passing a LoadOptions object when loading the document.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.That(doc.FirstSection.Body.FirstParagraph.GetText().Trim(), Is.EqualTo("Test encrypted document."));
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## Document(*string*) {#constructor_3}

Opens an existing document from a file. Automatically detects the file format.

```csharp
public Document(string fileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | File name of the document to open. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception/) | The document appears to be corrupted and cannot be loaded. |
| Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| ArgumentException | The name of the file cannot be null or empty string. |

## Examples

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

Shows how to load a PDF.

```csharp
Document doc = new Aspose.Words.Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

// Below are two ways of loading PDF documents using Aspose products.
// 1 -  Load as an Aspose.Words document:
Document asposeWordsDoc = new Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

Assert.That(asposeWordsDoc.GetText().Trim(), Is.EqualTo("Hello world!"));

// 2 -  Load as an Aspose.Pdf document:
Aspose.Pdf.Document asposePdfDoc = new Aspose.Pdf.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

TextFragmentAbsorber textFragmentAbsorber = new TextFragmentAbsorber();
asposePdfDoc.Pages.Accept(textFragmentAbsorber);

Assert.That(textFragmentAbsorber.Text.Trim(), Is.EqualTo("Hello world!"));
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## Document(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_4}

Opens an existing document from a file. Allows to specify additional options such as an encryption password.

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | File name of the document to open. |
| loadOptions | LoadOptions | Additional options to use when loading a document. Can be `null`. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception/) | The document appears to be corrupted and cannot be loaded. |
| Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| ArgumentException | The name of the file cannot be null or empty string. |

## Examples

Shows how to load an encrypted Microsoft Word document.

```csharp
Document doc;

// Aspose.Words throw an exception if we try to open an encrypted document without its password.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// When loading such a document, the password is passed to the document's constructor using a LoadOptions object.
LoadOptions options = new LoadOptions("docPassword");

// There are two ways of loading an encrypted document with a LoadOptions object.
// 1 -  Load the document from the local file system by filename:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 -  Load the document from a stream:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

Shows how to create and load documents.

```csharp
// There are two ways of creating a Document object using Aspose.Words.
// 1 -  Create a blank document:
Document doc = new Document();

// New Document objects by default come with the minimal set of nodes
// required to begin adding content such as text and shapes: a Section, a Body, and a Paragraph.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 -  Load a document that exists in the local file system:
doc = new Document(MyDir + "Document.docx");

// Loaded documents will have contents that we can access and edit.
Assert.That(doc.FirstSection.Body.FirstParagraph.GetText().Trim(), Is.EqualTo("Hello World!"));

// Some operations that need to occur during loading, such as using a password to decrypt a document,
// can be done by passing a LoadOptions object when loading the document.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.That(doc.FirstSection.Body.FirstParagraph.GetText().Trim(), Is.EqualTo("Test encrypted document."));
```

### See Also

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## Document(*Stream*) {#constructor_1}

Opens an existing document from a stream. Automatically detects the file format.

```csharp
public Document(Stream stream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | Stream where to load the document from. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception/) | The document appears to be corrupted and cannot be loaded. |
| Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| ArgumentNullException | The stream cannot be null. |
| NotSupportedException | The stream does not support reading or seeking. |
| ObjectDisposedException | The stream is a disposed object. |

## Remarks

The document must be stored at the beginning of the stream. The stream must support random positioning.

## Examples

Shows how to load a document using a stream.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.docx"))
{
    Document doc = new Document(stream);

    Assert.That(doc.GetText().Trim(), Is.EqualTo("Hello World!\r\rHello Word!\r\r\rHello World!"));
}
```

Shows how to load a document from a URL.

```csharp
// Create a URL that points to a Microsoft Word document.
const string url = "https://filesamples.com/samples/document/docx/sample3.docx";

// Download the document into a byte array, then load that array into a document using a memory stream.
using (HttpClient httpClient = new HttpClient())
{
    HttpResponseMessage response = httpClient.GetAsync(url).Result;
    byte[] dataBytes = response.Content.ReadAsByteArrayAsync().Result;

    using (MemoryStream byteStream = new MemoryStream(dataBytes))
    {
        Document doc = new Document(byteStream);

        // At this stage, we can read and edit the document's contents and then save it to the local file system.
        Assert.That(doc.FirstSection.Body.Paragraphs[3].GetText().Trim(), Is.EqualTo("There are eight section headings in this document. At the beginning, \"Sample Document\" is a level 1 heading. " +
                      "The main section headings, such as \"Headings\" and \"Lists\" are level 2 headings. " +
                        "The Tables section contains two sub-headings, \"Simple Table\" and \"Complex Table,\" which are both level 3 headings."));

        doc.Save(ArtifactsDir + "Document.LoadFromWeb.docx");
    }
}
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## Document(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_2}

Opens an existing document from a stream. Allows to specify additional options such as an encryption password.

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | The stream where to load the document from. |
| loadOptions | LoadOptions | Additional options to use when loading a document. Can be `null`. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception/) | The document appears to be corrupted and cannot be loaded. |
| Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| ArgumentNullException | The stream cannot be null. |
| NotSupportedException | The stream does not support reading or seeking. |
| ObjectDisposedException | The stream is a disposed object. |

## Remarks

The document must be stored at the beginning of the stream. The stream must support random positioning.

## Examples

Shows how to load an encrypted Microsoft Word document.

```csharp
Document doc;

// Aspose.Words throw an exception if we try to open an encrypted document without its password.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// When loading such a document, the password is passed to the document's constructor using a LoadOptions object.
LoadOptions options = new LoadOptions("docPassword");

// There are two ways of loading an encrypted document with a LoadOptions object.
// 1 -  Load the document from the local file system by filename:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 -  Load the document from a stream:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

Shows how to open an HTML document with images from a stream using a base URI.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Pass the URI of the base folder while loading it
    // so that any images with relative URIs in the HTML document can be found.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Verify that the first shape of the document contains a valid image.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.That(shape.IsImage, Is.True);
    Assert.That(shape.ImageData.ImageBytes, Is.Not.Null);
    Assert.That(ConvertUtil.PointToPixel(shape.Width), Is.EqualTo(32.0).Within(0.01));
    Assert.That(ConvertUtil.PointToPixel(shape.Height), Is.EqualTo(32.0).Within(0.01));
}
```

Shows how save a web page as a .docx file.

```csharp
const string url = "https://products.aspose.com/words/";

using (HttpClient client = new HttpClient())
{
    byte[] bytes = client.GetByteArrayAsync(url).GetAwaiter().GetResult();

    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // The URL is used again as a baseUri to ensure that any relative image paths are retrieved correctly.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Load the HTML document from stream and pass the LoadOptions object.
        Document doc = new Document(stream, options);

        // At this stage, we can read and edit the document's contents and then save it to the local file system.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

### See Also

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
