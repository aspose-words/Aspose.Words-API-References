---
title: TabStopCollection.GetIndexByPosition
linktitle: GetIndexByPosition
articleTitle: GetIndexByPosition
second_title: Aspose.Words для .NET
description: Откройте для себя метод TabStopCollection GetIndexByPosition, чтобы легко найти индекс табуляции в любой указанной точке. Идеально подходит для точного управления макетом!
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

Показывает, как найти позицию, чтобы узнать, существует ли там табуляция, и получить ее индекс.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// Добавьте позицию табуляции на расстоянии 30 мм.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// Результат "0", возвращаемый "GetIndexByPosition", подтверждает, что табуляция остановлена
// в 30 мм существует в этой коллекции и имеет индекс 0.
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// "-1", возвращаемый "GetIndexByPosition", подтверждает, что
// в этой коллекции нет позиции табуляции с позицией 60 мм.
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### Смотрите также

* class [TabStopCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
