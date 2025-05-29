---
title: MemoryFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „MemoryFontSource Type“, die Ihren Quellschrifttyp anzeigt und so Ihre Designpräzision und Kreativität steigert. Entfesseln Sie Ihr Schriftpotenzial!
type: docs
weight: 40
url: /de/net/aspose.words.fonts/memoryfontsource/type/
---
## MemoryFontSource.Type property

Gibt den Typ der Schriftartquelle zurück.

```csharp
public override FontSourceType Type { get; }
```

## Beispiele

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

* enum [FontSourceType](../../fontsourcetype/)
* class [MemoryFontSource](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
