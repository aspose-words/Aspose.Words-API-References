---
title: PdfSaveOptions.DownsampleOptions
linktitle: DownsampleOptions
articleTitle: DownsampleOptions
second_title: Aspose.Words för .NET
description: Upptäck PdfSaveOptions DownsampleOptions-egenskap för att anpassa PDF-kvaliteten och optimera filstorleken för bättre prestanda och tydlighet.
type: docs
weight: 110
url: /sv/net/aspose.words.saving/pdfsaveoptions/downsampleoptions/
---
## PdfSaveOptions.DownsampleOptions property

Gör det möjligt att ange nedprovningsalternativ.

```csharp
public DownsampleOptions DownsampleOptions { get; set; }
```

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

* class [DownsampleOptions](../../downsampleoptions/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
