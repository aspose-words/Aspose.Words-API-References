---
title: FontSourceType Enum
linktitle: FontSourceType
articleTitle: FontSourceType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Fonts.FontSourceType per una gestione efficiente delle sorgenti dei font. Ottimizza l'elaborazione dei tuoi documenti con opzioni di font flessibili.
type: docs
weight: 3420
url: /it/net/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enumeration

Specifica il tipo di origine del font.

```csharp
public enum FontSourceType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| FontFile | `0` | Un[`FileFontSource`](../filefontsource/) oggetto che rappresenta un singolo file di font. |
| FontsFolder | `1` | Un[`FolderFontSource`](../folderfontsource/) oggetto che rappresenta la cartella con i file dei font. |
| MemoryFont | `2` | Un[`MemoryFontSource`](../memoryfontsource/) oggetto che rappresenta un singolo font in memoria. |
| SystemFonts | `3` | Un[`SystemFontSource`](../systemfontsource/) oggetto che rappresenta tutti i font installati nel sistema. |
| FontStream | `4` | Un[`StreamFontSource`](../streamfontsource/) oggetto che rappresenta un flusso con dati di font. |

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
