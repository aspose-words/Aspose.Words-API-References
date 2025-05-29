---
title: ColorMode Enum
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Saving.ColorMode-enum för optimerad färgåtergivning. Förbättra ditt dokuments visuella attraktionskraft med exakta färginställningar.
type: docs
weight: 5600
url: /sv/net/aspose.words.saving/colormode/
---
## ColorMode enumeration

Anger hur färger återges.

```csharp
public enum ColorMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Normal | `0` | Rendering med omodifierade färger. |
| Grayscale | `1` | Rendering med färger i en rad grå nyanser från vitt till svart. |

## Exempel

Visar hur man ändrar bildfärg med egenskapen för att spara alternativ.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
// Ställ in egenskapen "ColorMode" till "Grayscale" för att rendera alla bilder från dokumentet i svartvitt.
// Storleken på utdatadokumentet kan vara större med den här inställningen.
// Ställ in egenskapen "ColorMode" till "Normal" för att rendera alla bilder i färg.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
