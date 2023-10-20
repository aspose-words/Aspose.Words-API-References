---
title: TabStopCollection.GetIndexByPosition
linktitle: GetIndexByPosition
articleTitle: GetIndexByPosition
second_title: Aspose.Words для .NET
description: TabStopCollection GetIndexByPosition метод. Получает индекс табуляции с указанной позицией в пунктах на С#.
type: docs
weight: 90
url: /ru/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

Получает индекс табуляции с указанной позицией в пунктах.

```csharp
public int GetIndexByPosition(double position)
```

## Примеры

Показывает, как найти позицию, чтобы увидеть, существует ли там позиция табуляции, и получить ее индекс.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// Добавляем позицию табуляции на отметке 30 мм.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// Результат «0», возвращаемый «GetIndexByPosition», подтверждает, что позиция табуляции
// at 30mm существует в этой коллекции и находится под индексом 0.
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// «-1», возвращаемый «GetIndexByPosition», подтверждает, что
// в этой коллекции нет позиции табуляции с позицией 60 мм.
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### Смотрите также

* class [TabStopCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
