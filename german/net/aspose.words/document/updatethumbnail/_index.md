---
title: Document.UpdateThumbnail
linktitle: UpdateThumbnail
articleTitle: UpdateThumbnail
second_title: Aspose.Words für .NET
description: Aktualisieren Sie die Miniaturansicht Ihres Dokuments mühelos mit unseren anpassbaren Optionen. Verbessern Sie Ihre Visualisierung und die Präsentation Ihres Dokuments noch heute!
type: docs
weight: 840
url: /de/net/aspose.words/document/updatethumbnail/
---
## UpdateThumbnail(*[ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)*) {#updatethumbnail_1}

Aktualisierungen[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) des Dokuments gemäß den angegebenen Optionen.

```csharp
public void UpdateThumbnail(ThumbnailGeneratingOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| options | ThumbnailGeneratingOptions | Die zu verwendenden Generierungsoptionen. |

## Bemerkungen

Die[`ThumbnailGeneratingOptions`](../../../aspose.words.rendering/thumbnailgeneratingoptions/) ermöglicht Ihnen, die Quelle der Miniaturansicht, die Größe und andere Optionen anzugeben. Wenn der Versuch, eine Miniaturansicht zu generieren, fehlschlägt, wird keine geändert.

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

* class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## UpdateThumbnail() {#updatethumbnail}

Aktualisierungen[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) des Dokuments mit Standardoptionen.

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

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
