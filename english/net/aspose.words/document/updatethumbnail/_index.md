---
title: Document.UpdateThumbnail
second_title: Aspose.Words for .NET API Reference
description: Document method. Updates Thumbnail of the document according to the specified options in C#.
type: docs
weight: 780
url: /net/aspose.words/document/updatethumbnail/
---
## UpdateThumbnail(ThumbnailGeneratingOptions) {#updatethumbnail_1}

Updates [`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) of the document according to the specified options.

```csharp
public void UpdateThumbnail(ThumbnailGeneratingOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| options | ThumbnailGeneratingOptions | The generating options to use. |

## Remarks

The [`ThumbnailGeneratingOptions`](../../../aspose.words.rendering/thumbnailgeneratingoptions/) allows you to specify the source of thumbnail, size and other options. If attempt to generate thumbnail fails, doesn't change one.

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

* class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* class [Document](../)
* namespace [Aspose.Words](../../document/)
* assembly [Aspose.Words](../../../)

---

## UpdateThumbnail() {#updatethumbnail}

Updates [`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) of the document using default options.

```csharp
public void UpdateThumbnail()
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

* class [Document](../)
* namespace [Aspose.Words](../../document/)
* assembly [Aspose.Words](../../../)
