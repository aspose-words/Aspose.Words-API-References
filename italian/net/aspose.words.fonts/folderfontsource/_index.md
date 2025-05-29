---
title: FolderFontSource Class
linktitle: FolderFontSource
articleTitle: FolderFontSource
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fonts.FolderFontSource, la soluzione ideale per gestire in modo efficiente i font TrueType. Migliora la tipografia dei tuoi documenti oggi stesso!
type: docs
weight: 3290
url: /it/net/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class

Rappresenta la cartella che contiene i file dei font TrueType.

Per saperne di più, visita il[Lavorare con i font](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public class FolderFontSource : FontSourceBase
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FolderFontSource](folderfontsource/#constructor)(*string, bool*) | Ctor. |
| [FolderFontSource](folderfontsource/#constructor_1)(*string, bool, int*) | Ctor. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [FolderPath](../../aspose.words.fonts/folderfontsource/folderpath/) { get; } | Percorso della cartella. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Restituisce la priorità della sorgente del font. |
| [ScanSubfolders](../../aspose.words.fonts/folderfontsource/scansubfolders/) { get; } | Determina se eseguire o meno la scansione delle sottocartelle. |
| override [Type](../../aspose.words.fonts/folderfontsource/type/) { get; } | Restituisce il tipo di origine del font. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Restituisce l'elenco dei font disponibili tramite questa sorgente. |

## Esempi

Mostra come utilizzare una cartella di sistema locale contenente i font come origine dei font.

```csharp
// Crea una sorgente font da una cartella che contiene file font.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Guarda anche

* class [FontSourceBase](../fontsourcebase/)
* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
