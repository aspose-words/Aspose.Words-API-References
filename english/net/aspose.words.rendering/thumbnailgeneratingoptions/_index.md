---
title: ThumbnailGeneratingOptions Class
linktitle: ThumbnailGeneratingOptions
articleTitle: ThumbnailGeneratingOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Rendering.ThumbnailGeneratingOptions class. Can be used to specify additional options when generating thumbnail for a document in C#.
type: docs
weight: 4510
url: /net/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class

Can be used to specify additional options when generating thumbnail for a document.

```csharp
public class ThumbnailGeneratingOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [ThumbnailGeneratingOptions](thumbnailgeneratingoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [GenerateFromFirstPage](../../aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/) { get; set; } | Specifies whether to generate thumbnail from first page of the document or first image. |
| [ThumbnailSize](../../aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/) { get; set; } | Size of generated thumbnail in pixels. Default is 600x900. |

## Remarks

User can call method [`UpdateThumbnail`](../../aspose.words/document/updatethumbnail/) to generate [`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) for a document.

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

* namespace [Aspose.Words.Rendering](../../aspose.words.rendering/)
* assembly [Aspose.Words](../../)
