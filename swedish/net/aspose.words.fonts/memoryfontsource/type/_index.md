---
title: MemoryFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words för .NET
description: Upptäck egenskapen MemoryFontSource Type som avslöjar din typsnittskälltyp, vilket förbättrar din designprecision och kreativitet. Frigör din typsnittspotential!
type: docs
weight: 40
url: /sv/net/aspose.words.fonts/memoryfontsource/type/
---
## MemoryFontSource.Type property

Returnerar typen av teckensnittskällan.

```csharp
public override FontSourceType Type { get; }
```

## Exempel

Visar hur man använder en byte-array med data från en teckensnittsfil som teckensnittskälla.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Se även

* enum [FontSourceType](../../fontsourcetype/)
* class [MemoryFontSource](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
