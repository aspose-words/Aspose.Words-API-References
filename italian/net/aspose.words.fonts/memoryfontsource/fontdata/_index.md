---
title: MemoryFontSource.FontData
linktitle: FontData
articleTitle: FontData
second_title: Aspose.Words per .NET
description: Scopri la proprietà FontData di MemoryFontSource per un'integrazione perfetta dei font binari. Migliora i tuoi progetti con soluzioni efficienti per la gestione dei font.
type: docs
weight: 30
url: /it/net/aspose.words.fonts/memoryfontsource/fontdata/
---
## MemoryFontSource.FontData property

Dati binari del font.

```csharp
public byte[] FontData { get; }
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

* class [MemoryFontSource](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
