---
title: StreamFontSource Class
linktitle: StreamFontSource
articleTitle: StreamFontSource
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fonts.StreamFontSource, la soluzione ideale per sorgenti di font di flusso personalizzate che migliorano la flessibilità e il design dei documenti.
type: docs
weight: 3470
url: /it/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

Classe base per la sorgente del font del flusso definito dall'utente.

Per saperne di più, visita il[Lavorare con i font](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public abstract class StreamFontSource : FontSourceBase,   
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | La chiave di questa sorgente nella cache. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Restituisce la priorità della sorgente del font. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | Restituisce il tipo di origine del font. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Restituisce l'elenco dei font disponibili tramite questa sorgente. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | Questo metodo dovrebbe aprire il flusso con i dati del font su richiesta. |

## Osservazioni

Per utilizzare la sorgente del font stream dovresti creare una classe derivata da`StreamFontSource` e fornire l'implementazione del[`OpenFontDataStream`](./openfontdatastream/) metodo.

[`OpenFontDataStream`](./openfontdatastream/)Il metodo può essere chiamato più volte. La prima volta verrà chiamato quando Aspose.Words analizza le sorgenti dei font fornite per ottenere l'elenco dei font disponibili. In seguito, potrà essere chiamato se il font viene utilizzato nel documento per analizzare i dati del font e incorporarli in alcuni formati di output.

`StreamFontSource` può essere utile perché consente di caricare i dati del font solo quando è necessario e di non memorizzarli in memoria per il[`FontSettings`](../fontsettings/) tutta la vita.

## Esempi

Mostra come caricare i font dallo stream.

```csharp
public void StreamFontSourceFileRendering()
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.SetFontsSources(new FontSourceBase[] {new StreamFontSourceFile()});

    DocumentBuilder builder = new DocumentBuilder();
    builder.Document.FontSettings = fontSettings;
    builder.Font.Name = "Kreon-Regular";
    builder.Writeln("Test aspose text when saving to PDF.");

    builder.Document.Save(ArtifactsDir + "FontSettings.StreamFontSourceFileRendering.pdf");
}

/// <summary>
/// Carica i dati del font solo quando necessario invece di memorizzarli nella memoria
/// per l'intera durata dell'oggetto "FontSettings".
/// </summary>
private class StreamFontSourceFile : StreamFontSource
{
    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Kreon-Regular.ttf");
    }
}
```

### Guarda anche

* class [FontSourceBase](../fontsourcebase/)
* interface [  ](../../global/%02  /)
* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
