---
title: ThumbnailGeneratingOptions.ThumbnailSize
linktitle: ThumbnailSize
articleTitle: ThumbnailSize
second_title: Aspose.Words für .NET
description: Entdecken Sie anpassbare Miniaturbildoptionen mit unserer Eigenschaft „ThumbnailSize“. Generieren Sie Miniaturbilder in perfekter Pixelgröße, standardmäßig 600 x 900 für eine optimale Anzeige!
type: docs
weight: 30
url: /de/net/aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/
---
## ThumbnailGeneratingOptions.ThumbnailSize property

Größe des generierten Miniaturbilds in Pixeln. Standard ist 600 x 900.

```csharp
public Size ThumbnailSize { get; set; }
```

## Beispiele

Zeigt, wie die Miniaturansicht eines Dokuments aktualisiert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Es gibt zwei Möglichkeiten, beim Speichern eines Dokuments im EPUB-Format ein Miniaturbild festzulegen.
// 1 - Verwenden Sie die erste Seite des Dokuments:
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 - Verwenden Sie das erste im Dokument gefundene Bild:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### Siehe auch

* class [ThumbnailGeneratingOptions](../)
* namensraum [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Montage [Aspose.Words](../../../)
