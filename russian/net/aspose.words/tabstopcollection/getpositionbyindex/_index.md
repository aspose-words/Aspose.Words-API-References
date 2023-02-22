---
title: TabStopCollection.GetPositionByIndex
second_title: Справочник по API Aspose.Words для .NET
description: TabStopCollection метод. Получает позицию в пунктах позиции табуляции по указанному индексу.
type: docs
weight: 100
url: /ru/net/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection.GetPositionByIndex method

Получает позицию (в пунктах) позиции табуляции по указанному индексу.

```csharp
public double GetPositionByIndex(int index)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | Int32 | Указатель в коллекции позиций табуляции. |

### Возвращаемое значение

Положение табуляции.

### Примеры

Показывает, как найти вкладку, остановиться по ее индексу и проверить ее положение.

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
* пространство имен [Aspose.Words](../../tabstopcollection/)
* сборка [Aspose.Words](../../../)


