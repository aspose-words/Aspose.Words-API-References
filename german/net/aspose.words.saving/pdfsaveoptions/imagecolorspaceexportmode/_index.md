---
title: PdfSaveOptions.ImageColorSpaceExportMode
linktitle: ImageColorSpaceExportMode
articleTitle: ImageColorSpaceExportMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ImageColorSpaceExportMode“ von PdfSaveOptions, um die Bildfarbauswahl in Ihren PDFs für eine beeindruckende visuelle Qualität und Konsistenz zu optimieren.
type: docs
weight: 190
url: /de/net/aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/
---
## PdfSaveOptions.ImageColorSpaceExportMode property

Gibt an, wie der Farbraum für die Bilder im PDF-Dokument ausgewählt wird.

```csharp
public PdfImageColorSpaceExportMode ImageColorSpaceExportMode { get; set; }
```

## Bemerkungen

Der Standardwert istAuto .

WennSimpleCmyk Wert angegeben ist, [`ImageCompression`](../imagecompression/) Option wird ignoriert und Für alle Bilder im Dokument wird die Flate-Komprimierung verwendet.

SimpleCmyk Wert wird beim Speichern im PDF/A-Format nicht unterstützt. Auto Stattdessen wird der Wert verwendet.

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

* enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
