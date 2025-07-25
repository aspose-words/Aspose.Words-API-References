---
title: LoadOptions.BaseUri
linktitle: BaseUri
articleTitle: BaseUri
second_title: Aspose.Words for .NET
description: Discover the LoadOptions BaseUri property to easily convert relative URIs to absolute ones in your documents. Enhance your URI management today!
type: docs
weight: 20
url: /net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be `null` or empty string. Default is `null`.

```csharp
public string BaseUri { get; set; }
```

## Remarks

This property is used to resolve relative URIs into absolute in the following cases:

1. When loading an HTML document from a stream and the document contains images with relative URIs and does not have a base URI specified in the BASE HTML element.
2. When saving a document to PDF and other formats, to retrieve images linked using relative URIs so the images can be saved into the output document.

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

    Assert.That(shape.IsImage, Is.True);
    Assert.That(shape.ImageData.ImageBytes, Is.Not.Null);
    Assert.That(ConvertUtil.PointToPixel(shape.Width), Is.EqualTo(32.0).Within(0.01));
    Assert.That(ConvertUtil.PointToPixel(shape.Height), Is.EqualTo(32.0).Within(0.01));
}
```

### See Also

* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
