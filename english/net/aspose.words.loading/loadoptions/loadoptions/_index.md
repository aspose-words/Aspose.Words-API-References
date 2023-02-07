---
title: LoadOptions.LoadOptions
second_title: Aspose.Words for .NET API Reference
description: Initializes a new instance of this class with default values.
type: docs
weight: 10
url: /net/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions() {#constructor}

Initializes a new instance of this class with default values.

```csharp
public LoadOptions()
```

## Examples

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

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### See Also

* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../loadoptions/)
* assembly [Aspose.Words](../../../)

---

## LoadOptions(string) {#constructor_2}

A shortcut to initialize a new instance of this class with the specified password to load an encrypted document.

```csharp
public LoadOptions(string password)
```

| Parameter | Type | Description |
| --- | --- | --- |
| password | String | The password to open an encrypted document. Can be `null` or empty string. |

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
```

### See Also

* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../loadoptions/)
* assembly [Aspose.Words](../../../)

---

## LoadOptions(LoadFormat, string, string) {#constructor_1}

A shortcut to initialize a new instance of this class with properties set to the specified values.

```csharp
public LoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parameter | Type | Description |
| --- | --- | --- |
| loadFormat | LoadFormat | The format of the document to be loaded. |
| password | String | The password to open an encrypted document. Can be `null` or empty string. |
| baseUri | String | The string that will be used to resolve relative URIs to absolute. Can be `null` or empty string. |

## Examples

Shows how save a web page as a .docx file.

```csharp
const string url = "https://www.aspose.com/";

using (HttpClient client = new HttpClient()) 
{
    var bytes = await client.GetByteArrayAsync(url);
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

Shows how to specify a base URI when opening an html document.

```csharp
// Suppose we want to load an .html document that contains an image linked by a relative URI
// while the image is in a different location. In that case, we will need to resolve the relative URI into an absolute one.
// We can provide a base URI using an HtmlLoadOptions object. 
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// While the image was broken in the input .html, our custom base URI helped us repair the link.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// This output document will display the image that was missing.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### See Also

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../loadoptions/)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
