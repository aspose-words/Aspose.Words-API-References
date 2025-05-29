---
title: ThumbnailGeneratingOptions.GenerateFromFirstPage
linktitle: GenerateFromFirstPage
articleTitle: GenerateFromFirstPage
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Option „GenerateFromFirstPage“ Miniaturansichten von der ersten Seite oder dem ersten Bild des Dokuments erstellt und so Ihren visuellen Inhalt mühelos verbessert.
type: docs
weight: 20
url: /de/net/aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/
---
## ThumbnailGeneratingOptions.GenerateFromFirstPage property

Gibt an, ob eine Miniaturansicht von der ersten Seite des Dokuments oder vom ersten Bild generiert werden soll.

```csharp
public bool GenerateFromFirstPage { get; set; }
```

## Bemerkungen

Standard ist`WAHR` , was bedeutet, dass die Miniaturansicht von der ersten Seite des Dokuments generiert wird. Wenn der Wert`FALSCH` und das Dokument kein Bild enthält, wird eine Miniaturansicht von der ersten Seite des Dokuments generiert.

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
