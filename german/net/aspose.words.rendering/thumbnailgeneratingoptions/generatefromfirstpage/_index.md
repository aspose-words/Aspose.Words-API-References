---
title: ThumbnailGeneratingOptions.GenerateFromFirstPage
second_title: Aspose.Words für .NET-API-Referenz
description: ThumbnailGeneratingOptions eigendom. Gibt an ob eine Miniaturansicht von der ersten Seite des Dokuments oder vom ersten Bild generiert werden soll.
type: docs
weight: 20
url: /de/net/aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/
---
## ThumbnailGeneratingOptions.GenerateFromFirstPage property

Gibt an, ob eine Miniaturansicht von der ersten Seite des Dokuments oder vom ersten Bild generiert werden soll.

```csharp
public bool GenerateFromFirstPage { get; set; }
```

### Bemerkungen

Standard ist`WAHR` , was bedeutet, dass eine Miniaturansicht von der ersten Seite des Dokuments generiert wird. Wenn der Wert lautet`FALSCH` und es gibt kein Bild im Dokument, wird eine Miniaturansicht von der ersten Seite des Dokuments generiert.

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


