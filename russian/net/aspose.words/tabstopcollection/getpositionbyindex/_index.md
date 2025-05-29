---
title: TabStopCollection.GetPositionByIndex
linktitle: GetPositionByIndex
articleTitle: GetPositionByIndex
second_title: Aspose.Words для .NET
description: Откройте для себя метод TabStopCollection GetPositionByIndex, чтобы легко находить позиции табуляции в пунктах по индексу. Оптимизируйте свой макет без усилий!
type: docs
weight: 100
url: /ru/net/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection.GetPositionByIndex method

Получает позицию (в пунктах) табуляции по указанному индексу.

```csharp
public double GetPositionByIndex(int index)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | Int32 | Индекс коллекции позиций табуляции. |

### Возвращаемое значение

Положение табуляции.

## Примеры

Показывает, как найти вкладку, остановиться на ее индексе и проверить ее положение.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

// Проверяем положение второй позиции табуляции в коллекции.
Assert.AreEqual(ConvertUtil.MillimeterToPoint(60), tabStops.GetPositionByIndex(1), 0.1d);
```

### Смотрите также

* class [TabStopCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
