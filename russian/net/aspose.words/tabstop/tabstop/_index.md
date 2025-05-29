---
title: TabStop
linktitle: TabStop
articleTitle: TabStop
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор TabStop, легко создавайте и настраивайте экземпляры для улучшения функциональности в ваших проектах. Повысьте эффективность кодирования сегодня!
type: docs
weight: 10
url: /ru/net/aspose.words/tabstop/tabstop/
---
## TabStop(*double*) {#constructor}

Инициализирует новый экземпляр этого класса.

```csharp
public TabStop(double position)
```

## Примеры

Показывает, как работать с набором позиций табуляции в документе.

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

// Каждый символ «табуляции» перемещает курсор конструктора в положение следующей позиции табуляции.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Каждый абзац получает свою коллекцию позиций табуляции, которая клонирует свои значения из коллекции позиций табуляции конструктора документов.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Коллекция позиций табуляции может указать нам на позиции TabStop до и после определенных позиций.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Мы можем очистить коллекцию позиций табуляции абзаца, чтобы вернуться к поведению табуляции по умолчанию.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Смотрите также

* class [TabStop](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## TabStop(*double, [TabAlignment](../../tabalignment/), [TabLeader](../../tableader/)*) {#constructor_1}

Инициализирует новый экземпляр этого класса.

```csharp
public TabStop(double position, TabAlignment alignment, TabLeader leader)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| position | Double | Положение табуляции в пунктах. |
| alignment | TabAlignment | А[`TabAlignment`](../../tabalignment/) значение that определяет выравнивание текста на данной позиции табуляции. |
| leader | TabLeader | А[`TabLeader`](../../tableader/) значение, которое определяет тип линии выноски, отображаемой под символом табуляции. |

## Примеры

Показывает, как работать с набором позиций табуляции в документе.

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

// Каждый символ «табуляции» перемещает курсор конструктора в положение следующей позиции табуляции.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Каждый абзац получает свою коллекцию позиций табуляции, которая клонирует свои значения из коллекции позиций табуляции конструктора документов.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Коллекция позиций табуляции может указать нам на позиции TabStop до и после определенных позиций.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Мы можем очистить коллекцию позиций табуляции абзаца, чтобы вернуться к поведению табуляции по умолчанию.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Смотрите также

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
