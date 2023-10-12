---
title: Class ThumbnailGeneratingOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Rendering.ThumbnailGeneratingOptions klas. Kann verwendet werden um beim Generieren einer Miniaturansicht für ein Dokument zusätzliche Optionen anzugeben.
type: docs
weight: 4600
url: /de/net/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class

Kann verwendet werden, um beim Generieren einer Miniaturansicht für ein Dokument zusätzliche Optionen anzugeben.

```csharp
public class ThumbnailGeneratingOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [ThumbnailGeneratingOptions](thumbnailgeneratingoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [GenerateFromFirstPage](../../aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/) { get; set; } | Gibt an, ob eine Miniaturansicht von der ersten Seite des Dokuments oder vom ersten Bild generiert werden soll. |
| [ThumbnailSize](../../aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/) { get; set; } | Größe des generierten Miniaturbilds in Pixel. Standard ist 600 x 900. |

### Bemerkungen

Benutzer kann Methode aufrufen[`UpdateThumbnail`](../../aspose.words/document/updatethumbnail/) um zu generieren[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) für ein Dokument.

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

* namensraum [Aspose.Words.Rendering](../../aspose.words.rendering/)
* Montage [Aspose.Words](../../)


