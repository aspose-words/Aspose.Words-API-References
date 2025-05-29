---
title: FixedPageSaveOptions.MetafileRenderingOptions
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words för .NET
description: Upptäck FixedPageSaveOptions MetafileRenderingOptions-egenskap för att anpassa och förbättra din metafilrendering för optimala resultat.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/
---
## FixedPageSaveOptions.MetafileRenderingOptions property

Gör det möjligt att ange renderingsalternativ för metafiler.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; set; }
```

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

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [FixedPageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
