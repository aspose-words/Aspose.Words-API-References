---
title: TabStopCollection Class
linktitle: TabStopCollection
articleTitle: TabStopCollection
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.TabStopCollection. Легко управляйте пользовательскими позициями табуляции для абзацев и стилей, улучшая точность форматирования документов.
type: docs
weight: 7060
url: /ru/net/aspose.words/tabstopcollection/
---
## TabStopCollection class

Коллекция[`TabStop`](../tabstop/) объекты, представляющие пользовательские вкладки для абзаца или стиля.

Чтобы узнать больше, посетите[Объектная модель документа Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) документальная статья.

```csharp
public class TabStopCollection : InternableComplexAttr
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/tabstopcollection/count/) { get; } | Получает количество позиций табуляции в коллекции. |
| [Item](../../aspose.words/tabstopcollection/item/) { get; } | Получает табуляцию по указанному индексу. (2 indexers) |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words/tabstopcollection/add/#add)(*[TabStop](../tabstop/)*) | Добавляет или заменяет позицию табуляции в коллекции. |
| [Add](../../aspose.words/tabstopcollection/add/#add_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | Добавляет или заменяет позицию табуляции в коллекции. |
| [After](../../aspose.words/tabstopcollection/after/)(*double*) | Устанавливает первую позицию табуляции справа от указанной позиции. |
| [Before](../../aspose.words/tabstopcollection/before/)(*double*) | Устанавливает первую позицию табуляции слева от указанной позиции. |
| [Clear](../../aspose.words/tabstopcollection/clear/)() | Удаляет все позиции табуляции. |
| override [Equals](../../aspose.words/tabstopcollection/equals/#equals_1)(*object*) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [Equals](../../aspose.words/tabstopcollection/equals/#equals)(*TabStopCollection*) | Определяет, является ли указанный`TabStopCollection` равен по значению текущему`TabStopCollection` . |
| override [GetHashCode](../../aspose.words/tabstopcollection/gethashcode/)() | Служит хэш-функцией для этого типа. |
| [GetIndexByPosition](../../aspose.words/tabstopcollection/getindexbyposition/)(*double*) | Получает индекс табуляции с указанной позицией в пунктах. |
| [GetPositionByIndex](../../aspose.words/tabstopcollection/getpositionbyindex/)(*int*) | Получает позицию (в пунктах) табуляции по указанному индексу. |
| [RemoveByIndex](../../aspose.words/tabstopcollection/removebyindex/)(*int*) | Удаляет позицию табуляции по указанному индексу из коллекции. |
| [RemoveByPosition](../../aspose.words/tabstopcollection/removebyposition/)(*double*) | Удаляет табуляцию в указанной позиции из коллекции. |

## Примечания

В документах Microsoft Word табуляция может быть определена в свойствах стиля абзаца или непосредственно в свойствах абзаца. Стиль может быть основан на другом стиле. Поэтому полный набор табуляций для данного объекта представляет собой комбинацию табуляций , определенных непосредственно для этого объекта, и табуляций, унаследованных от родительских стилей.

В Aspose.Words, когда вы получаете`TabStopCollection` для абзаца или стиля, он содержит только пользовательские позиции табуляции, определенные непосредственно для этого абзаца или стиля. Коллекция не включает позиции табуляции, определенные в родительских стилях, или позиции табуляции по умолчанию.

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

* class [InternableComplexAttr](../internablecomplexattr/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
