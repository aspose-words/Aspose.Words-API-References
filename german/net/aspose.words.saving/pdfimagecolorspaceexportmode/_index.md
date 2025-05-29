---
title: PdfImageColorSpaceExportMode Enum
linktitle: PdfImageColorSpaceExportMode
articleTitle: PdfImageColorSpaceExportMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words PdfImageColorSpaceExportMode, um die Bildfarbauswahl in Ihren PDF-Dokumenten für beeindruckende visuelle Darstellungen zu optimieren.
type: docs
weight: 6270
url: /de/net/aspose.words.saving/pdfimagecolorspaceexportmode/
---
## PdfImageColorSpaceExportMode enumeration

Gibt an, wie der Farbraum für die Bilder im PDF-Dokument ausgewählt wird.

```csharp
public enum PdfImageColorSpaceExportMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Auto | `0` | Aspose.Words wählt automatisch den am besten geeigneten Farbraum für jedes Bild aus. |
| SimpleCmyk | `1` | Aspose.Words konvertiert RGB-Bilder mithilfe einer einfachen Formel in den CMYK-Farbraum. |

## Beispiele

Zeigt, wie beim Exportieren in PDF ein anderer Farbraum für Bilder in einem Dokument festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Setzen Sie die Eigenschaft "ImageColorSpaceExportMode" auf "PdfImageColorSpaceExportMode.Auto", um Aspose.Words zu erhalten
// wählt automatisch den Farbraum für Bilder im Dokument aus, das in PDF konvertiert wird.
// In den meisten Fällen ist der Farbraum RGB.
// Setzen Sie die Eigenschaft „ImageColorSpaceExportMode“ auf „PdfImageColorSpaceExportMode.SimpleCmyk“
// um den CMYK-Farbraum für alle Bilder im gespeicherten PDF zu verwenden.
// Aspose.Words wendet auch die Flate-Komprimierung auf alle Bilder an und ignoriert den Wert der Eigenschaft „ImageCompression“.
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
