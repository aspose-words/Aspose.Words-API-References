---
title: DownsampleOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words för .NET
description: Optimera bildkvaliteten med egenskapen DownsampleOptions Resolution, som definierar de ideala pixlarna per tum för överlägsna nedsamplingsresultat.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/downsampleoptions/resolution/
---
## DownsampleOptions.Resolution property

Anger upplösningen i pixlar per tum som bilderna ska nedsamplas till.

```csharp
public int Resolution { get; set; }
```

## Anmärkningar

Standardvärdet är 220 ppi.

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

* class [DownsampleOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
