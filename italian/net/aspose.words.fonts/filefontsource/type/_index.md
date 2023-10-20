---
title: FileFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: FileFontSource Type proprietà. Restituisce il tipo di fonte del carattere in C#.
type: docs
weight: 40
url: /it/net/aspose.words.fonts/filefontsource/type/
---
## FileFontSource.Type property

Restituisce il tipo di fonte del carattere.

```csharp
public override FontSourceType Type { get; }
```

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

* enum [FontSourceType](../../fontsourcetype/)
* class [FileFontSource](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
