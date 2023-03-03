---
title: FontSourceBase.WarningCallback
linktitle: WarningCallback
second_title: Aspose.Words for .NET API Reference
description: FontSourceBase property. Called during processing of font source when an issue is detected that might result in formatting fidelity loss in C#.
type: docs
weight: 30
url: /net/aspose.words.fonts/fontsourcebase/warningcallback/
---
## FontSourceBase.WarningCallback property

Called during processing of font source when an issue is detected that might result in formatting fidelity loss.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Examples

Shows how to call warning callback when the font sources working with.

```csharp
public void FontSourceWarning()
{
    FontSettings settings = new FontSettings();
    settings.SetFontsFolder("bad folder?", false);

    FontSourceBase source = settings.GetFontsSources()[0];
    FontSourceWarningCollector callback = new FontSourceWarningCollector();
    source.WarningCallback = callback;

    // Get the list of fonts to call warning callback.
    IList<PhysicalFontInfo> fontInfos = source.GetAvailableFonts();

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Contains("Error loading font from the folder \"bad folder?\""));
}

private class FontSourceWarningCollector : IWarningCallback
{
    /// <summary>
    /// Called every time a warning occurs during processing of font source.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        FontSubstitutionWarnings.Warning(info);
    }

    public readonly WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

### See Also

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [FontSourceBase](../)
* namespace [Aspose.Words.Fonts](../../fontsourcebase/)
* assembly [Aspose.Words](../../../)
