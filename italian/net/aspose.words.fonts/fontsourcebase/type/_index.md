---
title: FontSourceBase.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: FontSourceBase Type proprietà. Restituisce il tipo di fonte del carattere in C#.
type: docs
weight: 20
url: /it/net/aspose.words.fonts/fontsourcebase/type/
---
## FontSourceBase.Type property

Restituisce il tipo di fonte del carattere.

```csharp
public abstract FontSourceType Type { get; }
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
* class [FontSourceBase](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
