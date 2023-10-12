---
title: TabStopCollection.RemoveByIndex
second_title: Справочник по API Aspose.Words для .NET
description: TabStopCollection метод. Удаляет позицию табуляции по указанному индексу из коллекции.
type: docs
weight: 110
url: /ru/net/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection.RemoveByIndex method

Удаляет позицию табуляции по указанному индексу из коллекции.

```csharp
public void RemoveByIndex(int index)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | Int32 | Индекс в коллекции позиций табуляции. |

### Примеры

Показывает, как выбрать позицию табуляции в документе по ее индексу и удалить ее.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

Assert.AreEqual(2, tabStops.Count);

// Удалить первую позицию табуляции.
tabStops.RemoveByIndex(0);

Assert.AreEqual(1, tabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.RemoveByIndex.docx");
```

### Смотрите также

* class [TabStopCollection](../)
* пространство имен [Aspose.Words](../../tabstopcollection/)
* сборка [Aspose.Words](../../../)


