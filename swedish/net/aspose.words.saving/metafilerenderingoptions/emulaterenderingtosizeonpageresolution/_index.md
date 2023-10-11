---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
second_title: Aspose.Words för .NET API Referens
description: MetafileRenderingOptions fast egendom. Hämtar eller ställer in upplösningen i pixlar per tum för emulering av metafilrendering till storleken på sidan.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

Hämtar eller ställer in upplösningen i pixlar per tum för emulering av metafilrendering till storleken på sidan.

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

### Anmärkningar

Detta alternativ används endast när[`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/) är satt till`Sann`.

Standardvärdet är 96. Detta är en standardskärmupplösning. Dvs metafilrendering kommer att emulera visningen av metafilen i MS Word med en 100% zoomfaktor.

### Exempel

Visar hur man visar metafilen enligt storleken på sidan.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Ställ in egenskapen "EmulateRenderingToSizeOnPage" till "true"
// för att emulera rendering enligt metafilstorleken på sidan.
// Ställ in egenskapen "EmulateRenderingToSizeOnPage" till "false"
// för att emulera metafilrendering till dess standardstorlek i pixlar.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### Se även

* class [MetafileRenderingOptions](../)
* namnutrymme [Aspose.Words.Saving](../../metafilerenderingoptions/)
* hopsättning [Aspose.Words](../../../)


