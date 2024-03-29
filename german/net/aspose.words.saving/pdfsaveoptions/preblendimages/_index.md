---
title: PdfSaveOptions.PreblendImages
linktitle: PreblendImages
articleTitle: PreblendImages
second_title: Aspose.Words für .NET
description: PdfSaveOptions PreblendImages eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt ob transparente Bilder mit schwarzer Hintergrundfarbe vorgemischt werden sollen oder nicht in C#.
type: docs
weight: 260
url: /de/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob transparente Bilder mit schwarzer Hintergrundfarbe vorgemischt werden sollen oder nicht.

```csharp
public bool PreblendImages { get; set; }
```

## Bemerkungen

Das Vormischen von Bildern kann das visuelle Erscheinungsbild von PDF-Dokumenten in Adobe Reader verbessern und Anti-Aliasing-Artefakte entfernen.

Um vorgemischte Bilder richtig anzuzeigen, muss die PDF-Viewer-Anwendung den Eintrag „/Matte“ im Softmask-Bildwörterbuch unterstützen. Auch das Vormischen von Bildern kann die PDF-Rendering-Leistung beeinträchtigen.

Der Standardwert ist`FALSCH`.

## Beispiele

Zeigt, wie man Bilder mit transparentem Hintergrund vormischt, während man ein Dokument als PDF speichert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „PreblendImages“ auf „true“, um transparente Bilder vorzumischen
// mit einem Hintergrund, der Artefakte reduzieren kann.
// Setzen Sie die Eigenschaft „PreblendImages“ auf „false“, um transparente Bilder normal darzustellen.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

Zeigt, wie Bilder mit transparentem Hintergrund vorgemischt werden (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „PreblendImages“ auf „true“, um transparente Bilder vorzumischen
// mit einem Hintergrund, der Artefakte reduzieren kann.
// Setzen Sie die Eigenschaft „PreblendImages“ auf „false“, um transparente Bilder normal darzustellen.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImagesNetStandard2.pdf", options);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
