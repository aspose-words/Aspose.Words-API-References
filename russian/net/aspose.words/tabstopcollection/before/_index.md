---
title: TabStopCollection.Before
second_title: Справочник по API Aspose.Words для .NET
description: TabStopCollection метод. Получает первую позицию табуляции слева от указанной позиции.
type: docs
weight: 50
url: /ru/net/aspose.words/tabstopcollection/before/
---
## TabStopCollection.Before method

Получает первую позицию табуляции слева от указанной позиции.

```csharp
public TabStop Before(double position)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| position | Double | Исходное положение (в пунктах). |

### Возвращаемое значение

Объект табуляции или`нулевой` если подходящая позиция табуляции не найдена.

### Примечания

Пропускает позиции табуляции с помощью[`Alignment`](../../tabstop/alignment/) установлен вBar.

### Примеры

Показывает, как работать с коллекцией табуляции документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 пункта — это один «дюйм» на линейке табуляции Microsoft Word.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Каждый символ табуляции переносит курсор компоновщика в место следующей позиции табуляции.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Каждый абзац получает свою коллекцию позиций табуляции, которая клонирует свои значения из коллекции позиций табуляции конструктора документов.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Коллекция табуляции может указывать нам на TabStops до и после определенных позиций.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Мы можем очистить коллекцию табуляции абзаца, чтобы вернуться к поведению табуляции по умолчанию.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Смотрите также

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* пространство имен [Aspose.Words](../../tabstopcollection/)
* сборка [Aspose.Words](../../../)


