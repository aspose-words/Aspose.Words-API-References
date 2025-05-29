---
title: PdfSaveOptions.PreblendImages
linktitle: PreblendImages
articleTitle: PreblendImages
second_title: Aspose.Words für .NET
description: Entdecken Sie die PreblendImages-Eigenschaft von PdfSaveOptions. Steuern Sie transparente Bildüberblendungen ganz einfach für eine verbesserte Dokumentqualität und visuelle Attraktivität.
type: docs
weight: 270
url: /de/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob transparente Bilder mit schwarzer Hintergrundfarbe vorgemischt werden sollen oder nicht.

```csharp
public bool PreblendImages { get; set; }
```

## Bemerkungen

Durch das Vormischen von Bildern kann die visuelle Darstellung von PDF-Dokumenten in Adobe Reader verbessert und Anti-Aliasing-Artefakte entfernt werden.

Um vorgemischte Bilder richtig anzuzeigen, muss die PDF-Viewer-Anwendung den Eintrag /Matte im Soft-Mask-Bildwörterbuch unterstützen. Außerdem kann das Vormischen von Bildern die Leistung des PDF-Renderings beeinträchtigen.

Der Standardwert ist`FALSCH`.

## Beispiele

Zeigt, wie Sie beim Speichern eines Dokuments im PDF-Format Bilder mit transparentem Hintergrund vormischen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();
// Setzen Sie die Eigenschaft „PreblendImages“ auf „true“, um transparente Bilder vorzublenden
// mit einem Hintergrund, der Artefakte reduzieren kann.
// Setzen Sie die Eigenschaft „PreblendImages“ auf „false“, um transparente Bilder normal zu rendern.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
