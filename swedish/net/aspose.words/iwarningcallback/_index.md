---
title: IWarningCallback Interface
linktitle: IWarningCallback
articleTitle: IWarningCallback
second_title: Aspose.Words för .NET
description: Implementera gränssnittet Aspose.Words.IWarningCallback för att anpassa metoder för att fånga upp varningar om tillförlitlighet vid inläsning och sparning av dokument. Förbättra dokumentintegriteten!
type: docs
weight: 3660
url: /sv/net/aspose.words/iwarningcallback/
---
## IWarningCallback interface

Implementera det här gränssnittet om du vill att din egen anpassade metod ska anropas för att fånga upp varningar om förlust av återgivning som kan uppstå vid inläsning eller sparning av dokument.

```csharp
public interface IWarningCallback
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Warning](../../aspose.words/iwarningcallback/warning/)(*[WarningInfo](../warninginfo/)*) | Aspose.Words anropar den här metoden när den stöter på problem under inläsning eller sparning av dokument, vilket kan leda till förlust av formatering eller dataåtergivning. |

## Exempel

Visar hur man använder IWarningCallback-gränssnittet för att övervaka varningar om teckensnittsersättning.

```csharp
public void SubstitutionWarning()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // Lagra den aktuella samlingen av teckensnittskällor, som kommer att vara standardteckensnittskällan för varje dokument
    // för vilka vi inte anger en annan teckensnittskälla.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // För teständamål kommer vi att ställa in Aspose.Words så att den bara letar efter teckensnitt i en mapp som inte finns.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // När dokumentet renderas kommer det inte att finnas någonstans att hitta teckensnittet "Times New Roman".
    // Detta kommer att orsaka en varning om teckensnittsersättning, vilket vår återanropsfunktion kommer att upptäcka.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].WarningType == WarningType.FontSubstitution);
    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// Anropas varje gång en varning uppstår under inläsning/sparning.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

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

Visar hur man ställer in egenskapen för att hitta den närmaste matchningen för ett saknat teckensnitt från de tillgängliga teckensnittskällorna.

```csharp
public void EnableFontSubstitution()
{
    // Öppna ett dokument som innehåller text formaterad med ett teckensnitt som inte finns i någon av våra teckensnittskällor.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Tilldela en återanropning för att hantera varningar om teckensnittsersättning.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Ange ett standardnamn för teckensnitt och aktivera teckensnittsersättning.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Ursprungliga teckensnittsmått bör användas efter teckensnittsersättning.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // Vi får en varning om teckensnittsersättning om vi sparar ett dokument med ett saknat teckensnitt.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // Vi kan också verifiera varningar i samlingen och rensa dem.
    Assert.AreEqual(WarningSource.Layout, substitutionWarningHandler.FontWarnings[0].Source);
    Assert.AreEqual(
        "Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
        substitutionWarningHandler.FontWarnings[0].Description);

    substitutionWarningHandler.FontWarnings.Clear();

    Assert.AreEqual(0, substitutionWarningHandler.FontWarnings.Count);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Anropas varje gång en varning uppstår under inläsning/sparning.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontWarnings.Warning(info);
    }

    public WarningInfoCollection FontWarnings = new WarningInfoCollection();
}
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
