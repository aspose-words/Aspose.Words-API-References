---
title: WarningCallback
second_title: Aspose.Words för .NET API Referens
description: Anropas under olika dokumentbehandlingsprocedurer när ett problem upptäcks som kan resultera i data eller formateringsförlust.
type: docs
weight: 90
url: /sv/net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

Anropas under olika dokumentbehandlingsprocedurer när ett problem upptäcks som kan resultera i data- eller formateringsförlust.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### Anmärkningar

Dokument kan generera varningar i vilket skede som helst av dess existens, så det är viktigt att ställa in varningsåteruppringning så så tidigt som möjligt för att undvika förlust av varningar. T ex sådana egenskaper som[`PageCount`](../../document/pagecount/) bygger faktiskt dokumentlayouten som används senare för rendering, och layoutvarningarna kan gå förlorade om varningsåteruppringning anges bara för renderingsanropen senare.

### Exempel

Visar hur man använder IWarningCallback-gränssnittet för att övervaka varningar för teckensnittsersättning.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // Lagra den aktuella samlingen av teckensnittskällor, som kommer att vara standardfontkällan för varje dokument
    // som vi inte anger en annan typsnittskälla för.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // För teständamål kommer vi att ställa in Aspose.Words att leta efter typsnitt endast i en mapp som inte finns.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // När du renderar dokumentet finns det ingen plats att hitta typsnittet "Times New Roman".
    // Detta kommer att orsaka en varning för teckensnittsersättning, som vår återuppringning kommer att upptäcka.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// Anropas varje gång en varning inträffar under laddning/sparning.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

Visar hur du ställer in egenskapen för att hitta den närmaste matchningen för ett saknat teckensnitt från tillgängliga teckensnittskällor.

```csharp
[Test]
public void EnableFontSubstitution()
{
    // Öppna ett dokument som innehåller text formaterad med ett teckensnitt som inte finns i någon av våra teckensnittskällor.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Tilldela en återuppringning för hantering av varningar för teckensnittsersättning.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Ange ett standardtypsnittsnamn och aktivera teckensnittsersättning.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Vi kommer att få en varning för ersättning av teckensnitt om vi sparar ett dokument med ett teckensnitt som saknas.
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

    Assert.That(substitutionWarningHandler.FontWarnings, Is.Empty);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Anropas varje gång en varning inträffar under laddning/sparning.
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

* interface [IWarningCallback](../../iwarningcallback/)
* class [DocumentBase](../)
* namnutrymme [Aspose.Words](../../documentbase/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
