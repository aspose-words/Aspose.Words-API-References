---
title: FontInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FontInfoCollection Count, с легкостью извлеките общее количество элементов в вашей коллекции для бесперебойного управления данными.
type: docs
weight: 10
url: /ru/net/aspose.words.fonts/fontinfocollection/count/
---
## FontInfoCollection.Count property

Получает количество элементов, содержащихся в коллекции.

```csharp
public int Count { get; }
```

## Примеры

Показывает информацию о шрифтах, присутствующих в пустом документе.

```csharp
Document doc = new Document();

// Пустой документ содержит 3 шрифта по умолчанию. Каждый шрифт в документе
// будет иметь соответствующий объект FontInfo, содержащий сведения об этом шрифте.
Assert.AreEqual(3, doc.FontInfos.Count);

Assert.True(doc.FontInfos.Contains("Times New Roman"));
Assert.AreEqual(204, doc.FontInfos["Times New Roman"].Charset);

Assert.True(doc.FontInfos.Contains("Symbol"));
Assert.True(doc.FontInfos.Contains("Arial"));
```

### Смотрите также

* class [FontInfoCollection](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
