---
title: FixedPageSaveOptions.ColorMode
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words für .NET
description: FixedPageSaveOptions ColorMode eigendom. Ruft einen Wert ab oder legt ihn fest der bestimmt wie Farben gerendert werden in C#.
type: docs
weight: 10
url: /de/net/aspose.words.saving/fixedpagesaveoptions/colormode/
---
## FixedPageSaveOptions.ColorMode property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie Farben gerendert werden.

```csharp
public ColorMode ColorMode { get; set; }
```

## Bemerkungen

Der Standardwert istNormal .

## Beispiele

Zeigt, wie man die Bildfarbe mit der Eigenschaft „Speicheroptionen“ ändert.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
// Setzen Sie die Eigenschaft „ColorMode“ auf „Grayscale“, um alle Bilder aus dem Dokument in Schwarzweiß darzustellen.
// Die Größe des Ausgabedokuments kann bei dieser Einstellung größer sein.
// Setzen Sie die Eigenschaft „ColorMode“ auf „Normal“, um alle Bilder in Farbe darzustellen.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Siehe auch

* enum [ColorMode](../../colormode/)
* class [FixedPageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
