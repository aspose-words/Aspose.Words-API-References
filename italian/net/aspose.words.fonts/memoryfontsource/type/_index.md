---
title: MemoryFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: Scopri la proprietà MemoryFontSource Type che rivela il tipo di sorgente del tuo font, migliorando la precisione e la creatività del tuo design. Sblocca il potenziale del tuo font!
type: docs
weight: 40
url: /it/net/aspose.words.fonts/memoryfontsource/type/
---
## MemoryFontSource.Type property

Restituisce il tipo di origine del font.

```csharp
public override FontSourceType Type { get; }
```

## Esempi

Mostra come utilizzare un array di byte con dati provenienti da un file di font come sorgente del font.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Guarda anche

* enum [FontSourceType](../../fontsourcetype/)
* class [MemoryFontSource](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
