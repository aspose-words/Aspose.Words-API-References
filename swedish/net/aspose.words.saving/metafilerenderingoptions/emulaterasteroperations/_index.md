---
title: MetafileRenderingOptions.EmulateRasterOperations
linktitle: EmulateRasterOperations
articleTitle: EmulateRasterOperations
second_title: Aspose.Words för .NET
description: MetafileRenderingOptions EmulateRasterOperations fast egendom. Hämtar eller ställer in ett värde som avgör om rasteroperationerna ska emuleras eller inte i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/
---
## MetafileRenderingOptions.EmulateRasterOperations property

Hämtar eller ställer in ett värde som avgör om rasteroperationerna ska emuleras eller inte.

```csharp
public bool EmulateRasterOperations { get; set; }
```

## Anmärkningar

Specifika rasteroperationer kan användas i metafiler. De kan inte renderas direkt till vektorgrafik. Att emulera rasteroperationer kräver partiell rasterisering av den resulterande vektorgrafiken, vilket kan påverka renderingsprestandan för metafil.

När detta värde är satt till`Sann`, Aspose.Words emulerar rasteroperationerna. Den resulterande utgången kanske är delvis rastrerad och prestandan kan vara långsammare.

När detta värde är satt till`falsk`, Aspose.Words emulerar inte rasteroperationerna. När Aspose.Words stöter på en rasteroperation i en metafil återgår den till att rendera metafilen till en bitmapp genom att använda operativsystemet .

Det här alternativet används endast när metafilen renderas som vektorgrafik.

Standardvärdet är`Sann`.

## Exempel

Visar lade till en reserv till bitmappsrendering och ändrade typ av varningar om metafilposter som inte stöds.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Ställ in egenskapen "EmulateRasterOperations" till "false" för att falla tillbaka till bitmapp när
    // den stöter på en metafil, som kräver rasteroperationer för att rendera i utdata-PDF.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Ställ in egenskapen "RenderingMode" till "VectorWithFallback" för att försöka rendera varje metafil med vektorgrafik.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
    // för att ändra hur den metoden konverterar dokumentet till .PDF och tillämpar konfigurationen
    // i vårt MetafileRenderingOptions-objekt mot sparoperationen.
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
/// Skriver ut och samlar in formateringsförlustrelaterade varningar som uppstår när ett dokument sparas.
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

* class [MetafileRenderingOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
