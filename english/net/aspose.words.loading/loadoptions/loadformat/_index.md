---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words for .NET
description: LoadOptions LoadFormat property. Specifies the format of the document to be loaded. Default is Auto in C#.
type: docs
weight: 90
url: /net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

Specifies the format of the document to be loaded. Default is Auto.

```csharp
public LoadFormat LoadFormat { get; set; }
```

## Remarks

It is recommended that you specify the Auto value and let Aspose.Words detect the file format automatically. If you know the format of the document you are about to load, you can specify the format explicitly and this will slightly reduce the loading time by the overhead associated with auto detecting the format. If you specify an explicit load format and it will turn out to be wrong, the auto detection will be invoked and a second attempt to load the file will be made.

## Examples

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
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
