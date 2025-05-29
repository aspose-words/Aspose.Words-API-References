---
title: MetafileRenderingOptions Class
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Saving.MetafileRenderingOptions för förbättrad kontroll och anpassning av metafilers rendering i dina dokument. Optimera ditt arbetsflöde idag!
type: docs
weight: 6080
url: /sv/net/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class

Gör det möjligt att ange ytterligare renderingsalternativ för metafiler.

För att lära dig mer, besök[Hantera Windows-metafiler](https://docs.aspose.com/words/net/handling-windows-metafiles/) dokumentationsartikel.

```csharp
public class MetafileRenderingOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [MetafileRenderingOptions](metafilerenderingoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [EmfPlusDualRenderingMode](../../aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur EMF+ Dual-metafiler ska renderas. |
| [EmulateRasterOperations](../../aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/) { get; set; } | Hämtar eller anger ett värde som avgör om rasteroperationerna ska emuleras eller inte. |
| [EmulateRenderingToSizeOnPage](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/) { get; set; } | Hämtar eller anger ett värde som avgör om metafilrendering emulerar visningen av metafilen enligt storleken på sidan eller visningen av metafilen i dess standardstorlek. |
| [EmulateRenderingToSizeOnPageResolution](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/) { get; set; } | Hämtar eller ställer in upplösningen i pixlar per tum för emulering av metafilrendering till storleken på sidan. |
| [RenderingMode](../../aspose.words.saving/metafilerenderingoptions/renderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur metafilbilder ska renderas. |
| [UseEmfEmbeddedToWmf](../../aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur WMF-metafiler med inbäddade EMF-metafiler ska renderas. |
| [UseGdiRasterOperationsEmulation](../../aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/) { get; set; } | Hämtar eller ställer in ett värde som avgör om GDI+ ska användas för rasteroperationsemulering. |

## Exempel

Program har lagt till en reservfunktion för bitmappsrendering och ändrat typen av varningar om metafilposter som inte stöds.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Sätt egenskapen "EmulateRasterOperations" till "false" för att återgå till bitmapp när
    // den stöter på en metafil, vilket kräver rasteroperationer för att renderas i utdata-PDF:en.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Sätt egenskapen "RenderingMode" till "VectorWithFallback" för att försöka rendera varje metafil med vektorgrafik.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
    // för att ändra hur den metoden konverterar dokumentet till .PDF och tillämpar konfigurationen
    // i vårt MetafileRenderingOptions-objekt till sparoperationen.
    PdfSaveOptions saveOptions = new PdfSaveOptions();
    saveOptions.MetafileRenderingOptions = metafileRenderingOptions;

    HandleDocumentWarnings callback = new HandleDocumentWarnings();
    doc.WarningCallback = callback;

    doc.Save(ArtifactsDir + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    Assert.AreEqual(1, callback.Warnings.Count);
    Assert.AreEqual("'R2_XORPEN' binary raster operation is not supported.",
        callback.Warnings[0].Description);
}

/// <summary>
/// Skriver ut och samlar in varningar om formateringsförlust som uppstår när ett dokument sparas.
/// </summary>
public class HandleDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.MinorFormattingLoss)
        {
            Console.WriteLine("Unsupported operation: " + info.Description);
            Warnings.Warning(info);
        }
    }

    public WarningInfoCollection Warnings = new WarningInfoCollection();
}
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
