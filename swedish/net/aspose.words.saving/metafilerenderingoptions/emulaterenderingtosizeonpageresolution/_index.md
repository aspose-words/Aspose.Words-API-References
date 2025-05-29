---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
linktitle: EmulateRenderingToSizeOnPageResolution
articleTitle: EmulateRenderingToSizeOnPageResolution
second_title: Aspose.Words för .NET
description: Upptäck egenskapen MetafileRenderingOptions EmulateRenderingToSizeOnPageResolution. Styr metafilrenderingsupplösningen för optimal sidvisning.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

Hämtar eller ställer in upplösningen i pixlar per tum för emulering av metafilrendering till storleken på sidan.

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

## Anmärkningar

Det här alternativet används endast när[`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/) är inställd på`sann`.

Standardvärdet är 96. Detta är en standardupplösning för skärmbilden. Dvs. metafilrendering kommer att emulera visningen av metafilen i MS Word med en zoomfaktor på 100 %.

## Exempel

Visar hur metafilen visas beroende på storleken på sidan.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Sätt egenskapen "EmulateRenderingToSizeOnPage" till "true"
// för att emulera rendering enligt metafilstorleken på sidan.
// Sätt egenskapen "EmulateRenderingToSizeOnPage" till "false"
// för att emulera metafilrendering till dess standardstorlek i pixlar.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### Se även

* class [MetafileRenderingOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
