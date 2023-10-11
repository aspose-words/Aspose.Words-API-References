---
title: ThumbnailGeneratingOptions.ThumbnailSize
second_title: Aspose.Words für .NET-API-Referenz
description: ThumbnailGeneratingOptions eigendom. Größe des generierten Miniaturbilds in Pixel. Standard ist 600 x 900.
type: docs
weight: 30
url: /de/net/aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/
---
## ThumbnailGeneratingOptions.ThumbnailSize property

Größe des generierten Miniaturbilds in Pixel. Standard ist 600 x 900.

```csharp
public Size ThumbnailSize { get; set; }
```

### Beispiele

Zeigt, wie die Miniaturansicht eines Dokuments aktualisiert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Es gibt zwei Möglichkeiten, ein Miniaturbild festzulegen, wenn ein Dokument im .epub-Format gespeichert wird.
// 1 – Die erste Seite des Dokuments verwenden:
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 – Das erste im Dokument gefundene Bild verwenden:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### Siehe auch

* class [ThumbnailGeneratingOptions](../)
* namensraum [Aspose.Words.Rendering](../../thumbnailgeneratingoptions/)
* Montage [Aspose.Words](../../../)


