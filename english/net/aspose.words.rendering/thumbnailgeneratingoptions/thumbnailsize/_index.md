---
title: ThumbnailGeneratingOptions.ThumbnailSize
linktitle: ThumbnailSize
second_title: Aspose.Words for .NET API Reference
description: ThumbnailGeneratingOptions ThumbnailSize property. Size of generated thumbnail in pixels. Default is 600x900 in C#.
type: docs
weight: 30
url: /net/aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/
---
## ThumbnailGeneratingOptions.ThumbnailSize property

Size of generated thumbnail in pixels. Default is 600x900.

```csharp
public Size ThumbnailSize { get; set; }
```

## Examples

Shows how to update a document's thumbnail.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// There are two ways of setting a thumbnail image when saving a document to .epub.
// 1 -  Use the document's first page:
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 -  Use the first image found in the document:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### See Also

* class [ThumbnailGeneratingOptions](../)
* namespace [Aspose.Words.Rendering](../../thumbnailgeneratingoptions/)
* assembly [Aspose.Words](../../../)
