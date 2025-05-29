---
title: ThumbnailGeneratingOptions Class
linktitle: ThumbnailGeneratingOptions
articleTitle: ThumbnailGeneratingOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Rendering.ThumbnailGeneratingOptions, um die Erstellung von Dokumentminiaturansichten mit anpassbaren Funktionen und verbesserter Qualität zu verbessern.
type: docs
weight: 5330
url: /de/net/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class

Kann verwendet werden, um zusätzliche Optionen beim Generieren einer Miniaturansicht für ein Dokument anzugeben.

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
| [ThumbnailSize](../../aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/) { get; set; } | Größe des generierten Miniaturbilds in Pixeln. Standard ist 600 x 900. |

## Bemerkungen

Benutzer kann Methode aufrufen[`UpdateThumbnail`](../../aspose.words/document/updatethumbnail/) um zu generieren[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) für ein Dokument.

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

* namensraum [Aspose.Words.Rendering](../../aspose.words.rendering/)
* Montage [Aspose.Words](../../)
