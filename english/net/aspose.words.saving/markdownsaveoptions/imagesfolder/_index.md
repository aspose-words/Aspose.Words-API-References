---
title: MarkdownSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words for .NET
description: Discover how the MarkdownSaveOptions ImagesFolder property enhances your document exports by specifying the ideal folder for saving images in Markdown format.
type: docs
weight: 80
url: /net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Specifies the physical folder where images are saved when exporting a document to the Markdown format. Default is an empty string.

```csharp
public string ImagesFolder { get; set; }
```

## Remarks

When you save a [`Document`](../../../aspose.words/document/) in Markdown format, Aspose.Words needs to save all images embedded in the document as standalone files. `ImagesFolder` allows you to specify where the images will be saved.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use `ImagesFolder` to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the `ImagesFolder` property.

If the folder specified by `ImagesFolder` doesn't exist, it will be created automatically.

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
