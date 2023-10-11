---
title: Enum ColorMode
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.ColorMode opsomming. Gibt an wie Farben gerendert werden.
type: docs
weight: 4860
url: /de/net/aspose.words.saving/colormode/
---
## ColorMode enumeration

Gibt an, wie Farben gerendert werden.

```csharp
public enum ColorMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Normal | `0` | Rendering mit unveränderten Farben. |
| Grayscale | `1` | Rendering mit Farben in verschiedenen Grautönen von Weiß bis Schwarz. |

### Beispiele

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


