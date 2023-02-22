---
title: FontSettings.DefaultInstance
second_title: Aspose.Words för .NET API Referens
description: FontSettings fast egendom. Statiska standardteckensnittsinställningar.
type: docs
weight: 20
url: /sv/net/aspose.words.fonts/fontsettings/defaultinstance/
---
## FontSettings.DefaultInstance property

Statiska standardteckensnittsinställningar.

```csharp
public static FontSettings DefaultInstance { get; }
```

### Anmärkningar

Denna instans används som standard i ett dokument om inte[`FontSettings`](../../../aspose.words/document/fontsettings/) anges.

### Exempel

Visar hur du konfigurerar standardtypsnittsinställningarna.

```csharp
// Konfigurera standardtypsnittsinställningarna för att använda typsnittet "Courier New".
// som backupersättning när vi försöker använda ett okänt teckensnitt.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.Enabled);

Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

// Det här dokumentet har ingen FontSettings-konfiguration. När vi återger dokumentet,
// standardinstansen FontSettings kommer att lösa det saknade teckensnittet.
// Aspose.Words kommer att använda "Courier New" för att återge text som använder det okända teckensnittet.
Assert.Null(doc.FontSettings);

doc.Save(ArtifactsDir + "FontSettings.DefaultFontInstance.pdf");
```

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

### Se även

* class [FontSettings](../)
* namnutrymme [Aspose.Words.Fonts](../../fontsettings/)
* hopsättning [Aspose.Words](../../../)


