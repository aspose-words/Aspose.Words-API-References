---
title: FileFontSource Class
linktitle: FileFontSource
articleTitle: FileFontSource
second_title: Aspose.Words per .NET
description: Aspose.Words.Fonts.FileFontSource classe. Rappresenta il singolo file di caratteri TrueType memorizzato nel file system in C#.
type: docs
weight: 2870
url: /it/net/aspose.words.fonts/filefontsource/
---
## FileFontSource class

Rappresenta il singolo file di caratteri TrueType memorizzato nel file system.

Per saperne di più, visita il[Lavorare con i caratteri](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public class FileFontSource : FontSourceBase
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FileFontSource](filefontsource/#constructor)(*string*) | Ctor. |
| [FileFontSource](filefontsource/#constructor_1)(*string, int*) | Ctor. |
| [FileFontSource](filefontsource/#constructor_2)(*string, int, string*) | Ctor. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/filefontsource/cachekey/) { get; } | La chiave di questa origine nella cache. |
| [FilePath](../../aspose.words.fonts/filefontsource/filepath/) { get; } | Percorso del file del carattere. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Restituisce la priorità della fonte del carattere. |
| override [Type](../../aspose.words.fonts/filefontsource/type/) { get; } | Restituisce il tipo di fonte del carattere. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Chiamato durante l'elaborazione dell'origine del carattere quando viene rilevato un problema che potrebbe comportare una perdita di fedeltà della formattazione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Restituisce l'elenco dei caratteri disponibili tramite questa origine. |

## Esempi

Mostra come utilizzare un file di font nel file system locale come origine di font.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Guarda anche

* class [FontSourceBase](../fontsourcebase/)
* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
