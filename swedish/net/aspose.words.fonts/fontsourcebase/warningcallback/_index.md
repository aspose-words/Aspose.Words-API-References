---
title: FontSourceBase.WarningCallback
second_title: Aspose.Words för .NET API Referens
description: FontSourceBase fast egendom. Anropas under bearbetning av teckensnittskällan när ett problem upptäcks som kan resultera i förlust av formatering.
type: docs
weight: 30
url: /sv/net/aspose.words.fonts/fontsourcebase/warningcallback/
---
## FontSourceBase.WarningCallback property

Anropas under bearbetning av teckensnittskällan när ett problem upptäcks som kan resultera i förlust av formatering.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### Exempel

Visar hur man ringer upp varningsåteruppringning när teckensnittskällorna arbetar med.

```csharp
public void FontSourceWarning()
{
    FontSettings settings = new FontSettings();
    settings.SetFontsFolder("bad folder?", false);

    FontSourceBase source = settings.GetFontsSources()[0];
    FontSourceWarningCollector callback = new FontSourceWarningCollector();
    source.WarningCallback = callback;

    // Hämta listan över teckensnitt att ringa tillbaka varning.
    IList<PhysicalFontInfo> fontInfos = source.GetAvailableFonts();

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Contains("Error loading font from the folder \"bad folder?\""));
}

private class FontSourceWarningCollector : IWarningCallback
{
    /// <summary>
    /// Anropas varje gång en varning inträffar under bearbetning av teckensnittskälla.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        FontSubstitutionWarnings.Warning(info);
    }

    public readonly WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

### Se även

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [FontSourceBase](../)
* namnutrymme [Aspose.Words.Fonts](../../fontsourcebase/)
* hopsättning [Aspose.Words](../../../)


