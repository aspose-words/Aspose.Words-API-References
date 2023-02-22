---
title: FileFontSource.FilePath
second_title: Aspose.Words per .NET API Reference
description: FileFontSource proprietà. Percorso del file del carattere.
type: docs
weight: 30
url: /it/net/aspose.words.fonts/filefontsource/filepath/
---
## FileFontSource.FilePath property

Percorso del file del carattere.

```csharp
public string FilePath { get; }
```

### Esempi

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

* class [FileFontSource](../)
* spazio dei nomi [Aspose.Words.Fonts](../../filefontsource/)
* assemblea [Aspose.Words](../../../)


