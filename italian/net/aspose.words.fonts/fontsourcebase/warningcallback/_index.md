---
title: FontSourceBase.WarningCallback
second_title: Aspose.Words per .NET API Reference
description: FontSourceBase proprietà. Chiamato durante lelaborazione dellorigine del carattere quando viene rilevato un problema che potrebbe causare una perdita di fedeltà di formattazione.
type: docs
weight: 30
url: /it/net/aspose.words.fonts/fontsourcebase/warningcallback/
---
## FontSourceBase.WarningCallback property

Chiamato durante l'elaborazione dell'origine del carattere quando viene rilevato un problema che potrebbe causare una perdita di fedeltà di formattazione.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### Esempi

Mostra come chiamare la richiamata di avviso quando funzionano le origini dei caratteri.

```csharp
[Test]
public void FontSourceWarning()
{
    FontSettings settings = new FontSettings();
    settings.SetFontsFolder("bad folder?", false);

    FontSourceBase source = settings.GetFontsSources()[0];
    FontSourceWarningCollector callback = new FontSourceWarningCollector();
    source.WarningCallback = callback;

    // Ottieni l'elenco dei caratteri per richiamare la richiamata di avviso.
    IList<PhysicalFontInfo> fontInfos = source.GetAvailableFonts();

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Contains("Error loading font from the folder \"bad folder?\""));
}

private class FontSourceWarningCollector : IWarningCallback
{
    /// <summary>
    /// Chiamato ogni volta che si verifica un avviso durante l'elaborazione della fonte del carattere.
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
* spazio dei nomi [Aspose.Words.Fonts](../../fontsourcebase/)
* assemblea [Aspose.Words](../../../)


