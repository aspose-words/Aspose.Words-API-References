---
title: FontSourceBase.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words per .NET
description: Scopri la proprietà FontSourceBase WarningCallback, essenziale per garantire la fedeltà della formattazione rilevando i problemi durante l'elaborazione della sorgente del font.
type: docs
weight: 30
url: /it/net/aspose.words.fonts/fontsourcebase/warningcallback/
---
## FontSourceBase.WarningCallback property

Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Esempi

Mostra come richiamare il callback di avviso quando le origini dei font funzionano con.

```csharp
public void FontSourceWarning()
{
    FontSettings settings = new FontSettings();
    settings.SetFontsFolder("bad folder?", false);

    FontSourceBase source = settings.GetFontsSources()[0];
    FontSourceWarningCollector callback = new FontSourceWarningCollector();
    source.WarningCallback = callback;

    // Ottieni l'elenco dei font per richiamare il callback di avviso.
    IList<PhysicalFontInfo> fontInfos = source.GetAvailableFonts();

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Contains("Error loading font from the folder \"bad folder?\""));
}

private class FontSourceWarningCollector : IWarningCallback
{
    /// <summary>
    /// Chiamato ogni volta che si verifica un avviso durante l'elaborazione della sorgente del font.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        FontSubstitutionWarnings.Warning(info);
    }

    public readonly WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

### Guarda anche

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [FontSourceBase](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
