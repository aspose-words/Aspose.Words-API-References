---
title: FontSettings.DefaultInstance
linktitle: DefaultInstance
articleTitle: DefaultInstance
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FontSettings DefaultInstance för effektiv hantering av statiska teckensnitt. Optimera din design med anpassningsbara standardinställningar!
type: docs
weight: 20
url: /sv/net/aspose.words.fonts/fontsettings/defaultinstance/
---
## FontSettings.DefaultInstance property

Statiska standardinställningar för teckensnitt.

```csharp
public static FontSettings DefaultInstance { get; }
```

## Anmärkningar

Den här instansen används som standard i ett dokument om inte[`FontSettings`](../../../aspose.words/document/fontsettings/) är specificerad.

## Exempel

Visar hur man konfigurerar standardinställningarna för teckensnitt.

```csharp
// Konfigurera standardinstansen för teckensnittsinställningar för att använda teckensnittet "Courier New"
// som en reserversättning när vi försöker använda ett okänt teckensnitt.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.Enabled);

Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

// Detta dokument har ingen FontSettings-konfiguration. När vi renderar dokumentet,
// standardinstansen FontSettings löser det saknade teckensnittet.
// Aspose.Words kommer att använda "Courier New" för att rendera text som använder det okända teckensnittet.
Assert.Null(doc.FontSettings);

doc.Save(ArtifactsDir + "FontSettings.DefaultFontInstance.pdf");
```

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

### Se även

* class [FontSettings](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
