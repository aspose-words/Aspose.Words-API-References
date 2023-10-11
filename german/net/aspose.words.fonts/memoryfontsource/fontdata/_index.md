---
title: MemoryFontSource.FontData
second_title: Aspose.Words für .NET-API-Referenz
description: MemoryFontSource eigendom. Binäre Schriftartdaten.
type: docs
weight: 30
url: /de/net/aspose.words.fonts/memoryfontsource/fontdata/
---
## MemoryFontSource.FontData property

Binäre Schriftartdaten.

```csharp
public byte[] FontData { get; }
```

### Beispiele

Zeigt, wie ein Byte-Array mit Daten aus einer Schriftartdatei als Schriftartquelle verwendet wird.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Siehe auch

* class [MemoryFontSource](../)
* namensraum [Aspose.Words.Fonts](../../memoryfontsource/)
* Montage [Aspose.Words](../../../)


