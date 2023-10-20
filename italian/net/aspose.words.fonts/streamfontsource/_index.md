---
title: StreamFontSource Class
linktitle: StreamFontSource
articleTitle: StreamFontSource
second_title: Aspose.Words per .NET
description: Aspose.Words.Fonts.StreamFontSource classe. Classe base per lorigine del carattere stream definito dallutente in C#.
type: docs
weight: 3040
url: /it/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

Classe base per l'origine del carattere stream definito dall'utente.

Per saperne di più, visita il[Lavorare con i caratteri](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public abstract class StreamFontSource : FontSourceBase
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | La chiave di questa origine nella cache. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Restituisce la priorità della fonte del carattere. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | Restituisce il tipo di fonte del carattere. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Chiamato durante l'elaborazione dell'origine del carattere quando viene rilevato un problema che potrebbe comportare una perdita di fedeltà della formattazione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Restituisce l'elenco dei caratteri disponibili tramite questa origine. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | Questo metodo dovrebbe aprire lo stream con i dati dei caratteri su richiesta. |

## Osservazioni

Per utilizzare l'origine del carattere del flusso è necessario creare una classe derivata dal file`StreamFontSource` e fornire l'implementazione di[`OpenFontDataStream`](./openfontdatastream/) metodo.

[`OpenFontDataStream`](./openfontdatastream/)il metodo potrebbe essere chiamato più volte. Per la prima volta verrà chiamato quando Aspose.Words esegue la scansione delle fonti di caratteri fornite per ottenere l'elenco dei caratteri disponibili. Successivamente potrebbe essere chiamato se il carattere viene utilizzato nel documento per analizzare i dati del carattere e incorporare i dati del carattere in alcuni formati di output.

`StreamFontSource` può essere utile perché permette di caricare i dati del font solo quando è richiesto e non di salvarli in memoria per il[`FontSettings`](../fontsettings/) tutta la vita.

## Esempi

Mostra come caricare i caratteri dallo stream.

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
/// Carica i dati dei caratteri solo quando richiesto invece di archiviarli nella memoria
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
* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
