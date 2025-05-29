---
title: FontSourceBase Class
linktitle: FontSourceBase
articleTitle: FontSourceBase
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.Fonts.FontSourceBase, la classe astratta essenziale per definire diverse sorgenti di font nelle tue applicazioni. Migliora la formattazione dei tuoi documenti!
type: docs
weight: 3410
url: /it/net/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class

Questa è una classe base astratta per le classi che consentono all'utente di specificare varie sorgenti di font.

Per saperne di più, visita il[Lavorare con i font](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public abstract class FontSourceBase
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Restituisce la priorità della sorgente del font. |
| abstract [Type](../../aspose.words.fonts/fontsourcebase/type/) { get; } | Restituisce il tipo di origine del font. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Restituisce l'elenco dei font disponibili tramite questa sorgente. |

## Esempi

Mostra come utilizzare un file di font nel file system locale come origine del font.

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

* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
