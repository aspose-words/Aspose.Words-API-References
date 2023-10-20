---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
linktitle: EmulateRenderingToSizeOnPage
articleTitle: EmulateRenderingToSizeOnPage
second_title: Aspose.Words för .NET
description: MetafileRenderingOptions EmulateRenderingToSizeOnPage fast egendom. Hämtar eller ställer in ett värde som avgör om metafilrendering emulerar visningen av metafilen enligt storleken på page eller visningen av metafilen i dess standardstorlek i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

Hämtar eller ställer in ett värde som avgör om metafil-rendering emulerar visningen av metafilen enligt storleken på page eller visningen av metafilen i dess standardstorlek.

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

## Anmärkningar

När metafiler visas i MS Word kan en del grafik skalas enligt den faktiska metafilstorleken i pixlar. Dvs även zoomning kan påverka metafilvisningen.

När detta värde är satt till`Sann` Aspose.Words emulerar rendering enligt metafilstorleken på sidan. Storleken i pixlar beräknas från metafilstorleken på sidan och den angivna[`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/).

När detta värde är satt till`falsk`, Aspose.Words emulerar metafil-rendering till dess standardstorlek i pixlar.

Det här alternativet används endast när metafilen renderas som vektorgrafik.

Standardvärdet är`Sann`.

## Exempel

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
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
