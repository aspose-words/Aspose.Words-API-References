---
title: TabStopCollection.RemoveByIndex
linktitle: RemoveByIndex
articleTitle: RemoveByIndex
second_title: Aspose.Words для .NET
description: Легко управляйте своими табуляторами с помощью метода RemoveByIndex. Быстро удаляйте любые табуляторы из своей коллекции для упрощения дизайна.
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
| index | Int32 | Индекс коллекции позиций табуляции. |

## Примеры

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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
