---
title: MetafileRenderingMode Enum
linktitle: MetafileRenderingMode
articleTitle: MetafileRenderingMode
second_title: Aspose.Words för .NET
description: Upptäck hur Aspose.Words.Saving.MetafileRenderingMode förbättrar WMF- och EMF-metafilrendering för optimal dokumentkvalitet och prestanda.
type: docs
weight: 6070
url: /sv/net/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enumeration

Anger hur Aspose.Words ska rendera WMF- och EMF-metafiler.

```csharp
public enum MetafileRenderingMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| VectorWithFallback | `0` | Aspose.Words försöker rendera en metafil som vektorgrafik. Om Aspose.Words inte kan rendera några av metafilposterna korrekt till vektorgrafik, renderar Aspose.Words denna metafil till en bitmapp. |
| Vector | `1` | Aspose.Words renderar en metafil som vektorgrafik. |
| Bitmap | `2` | Aspose.Words anropar GDI+ för att rendera en metafil till en bitmapp och sparar sedan bitmappen i utdatadokumentet. |

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
