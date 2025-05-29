---
title: DownsampleOptions Class
linktitle: DownsampleOptions
articleTitle: DownsampleOptions
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Saving.DownsampleOptions för att enkelt anpassa bildnedsampling för optimerad dokumentkvalitet och prestanda.
type: docs
weight: 5720
url: /sv/net/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class

Gör det möjligt att ange nedprovningsalternativ.

För att lära dig mer, besök[Spara ett dokument](https://docs.aspose.com/words/net/save-a-document/) dokumentationsartikel.

```csharp
public class DownsampleOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [DownsampleOptions](downsampleoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DownsampleImages](../../aspose.words.saving/downsampleoptions/downsampleimages/) { get; set; } | Anger om bilder ska nedsamplas. |
| [Resolution](../../aspose.words.saving/downsampleoptions/resolution/) { get; set; } | Anger upplösningen i pixlar per tum som bilderna ska nedsamplas till. |
| [ResolutionThreshold](../../aspose.words.saving/downsampleoptions/resolutionthreshold/) { get; set; } | Anger tröskelupplösningen i pixlar per tum. Om upplösningen för en bild i dokumentet är lägre än tröskelvärdet, kommer nedsamplingsalgoritmen inte att tillämpas. Ett värde på 0 innebär att tröskelkontrollen inte används och alla bilder som kan minskas i storlek nedsamplas. |

## Exempel

Visar hur man ändrar upplösningen på bilder i PDF-dokumentet.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Som standard nedsamplar Aspose.Words alla bilder i ett dokument som vi sparar till PDF till 220 ppi.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Sätt egenskapen "Upplösning" till "36" för att nedsampla alla bilder till 36 ppi.
options.DownsampleOptions.Resolution = 36;

// Ställ in egenskapen "ResolutionThreshold" för att endast tillämpa nedsampling på
// bilder med en upplösning som är över 128 ppi.
options.DownsampleOptions.ResolutionThreshold = 128;

// Endast de två första bilderna från dokumentet kommer att nedsamplas i detta skede.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
