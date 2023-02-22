---
title: FontSourceBase.WarningCallback
second_title: Aspose.Words für .NET-API-Referenz
description: FontSourceBase eigendom. Wird während der Verarbeitung der Schriftartquelle aufgerufen wenn ein Problem erkannt wird das zu einem Verlust der Formatierungstreue führen kann.
type: docs
weight: 30
url: /de/net/aspose.words.fonts/fontsourcebase/warningcallback/
---
## FontSourceBase.WarningCallback property

Wird während der Verarbeitung der Schriftartquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungstreue führen kann.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### Beispiele

Zeigt, wie man einen Warnrückruf aufruft, wenn die Schriftquellen mit arbeiten.

```csharp
[Test]
public void FontSourceWarning()
{
    FontSettings settings = new FontSettings();
    settings.SetFontsFolder("bad folder?", false);

    FontSourceBase source = settings.GetFontsSources()[0];
    FontSourceWarningCollector callback = new FontSourceWarningCollector();
    source.WarningCallback = callback;

    // Holen Sie sich die Liste der Schriftarten, um den Warnungsrückruf aufzurufen.
    IList<PhysicalFontInfo> fontInfos = source.GetAvailableFonts();

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Contains("Error loading font from the folder \"bad folder?\""));
}

private class FontSourceWarningCollector : IWarningCallback
{
    /// <summary>
    /// Wird jedes Mal aufgerufen, wenn während der Verarbeitung der Schriftartquelle eine Warnung auftritt.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        FontSubstitutionWarnings.Warning(info);
    }

    public readonly WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

### Siehe auch

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [FontSourceBase](../)
* namensraum [Aspose.Words.Fonts](../../fontsourcebase/)
* Montage [Aspose.Words](../../../)


