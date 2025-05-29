---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
linktitle: EmulateRenderingToSizeOnPage
articleTitle: EmulateRenderingToSizeOnPage
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen EmulateRenderingToSizeOnPage förbättrar metafilrendering och säkerställer korrekta visningsstorlekar för optimala visuella resultat.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

Hämtar eller anger ett värde som avgör om metafilrendering emulerar visningen av metafilen enligt storleken på sidan eller visningen av metafilen i dess standardstorlek.

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

## Anmärkningar

När metafiler visas i MS Word kan vissa bilder skalas enligt den faktiska metafilstorleken i pixlar. Dvs. även zoomning kan påverka metafilvisningen.

När detta värde är inställt på`sann`Aspose.Words emulerar rendering enligt metafilstorleken på sidan. Storleken i pixlar beräknas utifrån metafilstorleken på sidan och den angivna[`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/).

När detta värde är inställt på`falsk`Aspose.Words emulerar metafilrendering till dess standardstorlek i pixlar.

Det här alternativet används endast när metafilen återges som vektorgrafik.

Standardvärdet är`sann`.

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
