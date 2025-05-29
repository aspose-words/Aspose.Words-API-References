---
title: Font.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font LineSpacing, которое обеспечивает точный межстрочный интервал в пунктах, улучшая читаемость и дизайн текста.
type: docs
weight: 190
url: /ru/net/aspose.words/font/linespacing/
---
## Font.LineSpacing property

Возвращает межстрочный интервал данного шрифта (в пунктах).

```csharp
public double LineSpacing { get; }
```

## Примеры

Показывает, как получить межстрочный интервал шрифта в пунктах.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Установите разные шрифты для DocumentBuilder и проверьте их межстрочный интервал.
builder.Font.Name = "Calibri";
Assert.AreEqual(14.6484375d, builder.Font.LineSpacing);

builder.Font.Name = "Times New Roman";
Assert.AreEqual(13.798828125d, builder.Font.LineSpacing);
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
