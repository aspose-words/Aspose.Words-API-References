---
title: MemoryFontSource.FontData
linktitle: FontData
articleTitle: FontData
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FontData MemoryFontSource для бесшовной интеграции бинарных шрифтов. Улучшите свои проекты с помощью эффективных решений по управлению шрифтами.
type: docs
weight: 30
url: /ru/net/aspose.words.fonts/memoryfontsource/fontdata/
---
## MemoryFontSource.FontData property

Двоичные данные шрифта.

```csharp
public byte[] FontData { get; }
```

## Примеры

Показывает, как использовать байтовый массив с данными из файла шрифта в качестве источника шрифта.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Смотрите также

* class [MemoryFontSource](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
