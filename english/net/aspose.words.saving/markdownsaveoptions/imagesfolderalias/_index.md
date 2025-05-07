---
title: MarkdownSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words for .NET
description: Discover the MarkdownSaveOptions ImagesFolderAlias property to easily manage image URIs in your documents. Streamline your workflow with this essential feature!
type: docs
weight: 90
url: /net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

Specifies the name of the folder used to construct image URIs written into a document. Default is an empty string.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Remarks

When you save a [`Document`](../../../aspose.words/document/) in Markdown format, Aspose.Words needs to save all images embedded in the document as standalone files. [`ImagesFolder`](../imagesfolder/) allows you to specify where the images will be saved and `ImagesFolderAlias` allows to specify how the image URIs will be constructed.

If `ImagesFolderAlias` is not an empty string, then the image URI written to Markdown will be ImagesFolderAlias + &lt;image file name&gt;.

If `ImagesFolderAlias` is an empty string, then the image URI written to Markdown will be ImagesFolder + &lt;image file name&gt;.

If `ImagesFolderAlias` is set to '.' (dot), then the image file name will be written to Markdown without path regardless of other options.

## Examples

Shows how to specifies the name of the folder used to construct image URIs.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
builder.InsertImage(ImageDir + "Logo.jpg");

string imagesFolder = Path.Combine(ArtifactsDir, "ImagesDir");
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Use the "ImagesFolder" property to assign a folder in the local file system into which
// Aspose.Words will save all the document's linked images.
saveOptions.ImagesFolder = imagesFolder;
// Use the "ImagesFolderAlias" property to use this folder
// when constructing image URIs instead of the images folder's name.
saveOptions.ImagesFolderAlias = "http://example.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### See Also

* class [MarkdownSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
