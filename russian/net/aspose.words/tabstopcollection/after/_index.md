---
title: TabStopCollection.After
second_title: Справочник по API Aspose.Words для .NET
description: TabStopCollection метод. Получает первую позицию табуляции справа от указанной позиции.
type: docs
weight: 40
url: /ru/net/aspose.words/tabstopcollection/after/
---
## TabStopCollection.After method

Получает первую позицию табуляции справа от указанной позиции.

```csharp
public TabStop After(double position)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| position | Double | Контрольная позиция (в пунктах). |

### Возвращаемое значение

Объект табуляции или нуль, если подходящая табуляция не найдена.

### Примечания

Пропускает позиции табуляции с помощью **Выравнивание** установлен в`TabAlignment.Bar`.

### Примеры

Показывает, как работать с набором позиций табуляции в документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 точки — это один «дюйм» на линейке табуляции Microsoft Word.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Каждый символ табуляции переводит курсор конструктора в положение следующей позиции табуляции.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Каждый абзац получает свою коллекцию табуляции, которая клонирует свои значения из коллекции табуляции конструктора документов.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Набор позиций табуляции может указывать нам на позиции TabStop до и после определенных позиций.
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


