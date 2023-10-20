---
title: Document.UpdateThumbnail
linktitle: UpdateThumbnail
articleTitle: UpdateThumbnail
second_title: Aspose.Words für .NET
description: Document UpdateThumbnail methode. UpdatesThumbnail des Dokuments gemäß den angegebenen Optionen in C#.
type: docs
weight: 780
url: /de/net/aspose.words/document/updatethumbnail/
---
## UpdateThumbnail(*[ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)*) {#updatethumbnail_1}

Updates[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) des Dokuments gemäß den angegebenen Optionen.

```csharp
public void UpdateThumbnail(ThumbnailGeneratingOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| options | ThumbnailGeneratingOptions | Die zu verwendenden Generierungsoptionen. |

## Bemerkungen

Die[`ThumbnailGeneratingOptions`](../../../aspose.words.rendering/thumbnailgeneratingoptions/) Ermöglicht Ihnen, die Quelle des Miniaturbilds, die Größe und andere Optionen anzugeben. Wenn der Versuch, ein Miniaturbild zu generieren, fehlschlägt, wird eines nicht geändert.

## Beispiele

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

* class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## UpdateThumbnail() {#updatethumbnail}

Updates[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) des Dokuments mit Standardoptionen.

```csharp
public void UpdateThumbnail()
```

## Beispiele

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

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
