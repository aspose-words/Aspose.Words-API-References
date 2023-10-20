---
title: DocumentBuilder.MoveToBookmark
linktitle: MoveToBookmark
articleTitle: MoveToBookmark
second_title: Aspose.Words для .NET
description: DocumentBuilder MoveToBookmark метод. Перемещает курсор на закладку на С#.
type: docs
weight: 490
url: /ru/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(*string*) {#movetobookmark}

Перемещает курсор на закладку.

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | String | Имя закладки, на которую нужно переместить курсор. |

### Возвращаемое значение

`истинный` если закладка была найдена;`ЛОЖЬ` в противном случае.

## Примечания

Перемещает курсор в позицию сразу после начала закладки с указанным именем .

Сравнение не учитывает регистр. Если закладка не найдена,`ЛОЖЬ` is возвращается, а курсор не перемещается.

Вставка нового текста не заменяет существующий текст закладки.

Обратите внимание, что некоторые закладки в документе закреплены за полями формы. Переход к такой закладке и вставка туда текста вставляет текст в код поля формы . Хотя это не приведет к аннулированию поля формы, текст Insert не будет виден, поскольку он станет частью кода поля.

## Примеры

Показывает, как перемещать курсор построителя документов в разные узлы документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создать действительную закладку, объект, состоящий из узлов, заключенных в начальный узел закладки,
 // и конечный узел закладки.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Курсор конструктора документов всегда находится перед узлом, который мы в последний раз добавляли с его помощью.
// Если курсор компоновщика находится в конце документа, его текущий узел будет нулевым.
// Предыдущий узел — это конечный узел закладки, который мы добавили последним.
// Добавление новых узлов с помощью компоновщика добавит их к последнему узлу.
Assert.Null(builder.CurrentNode);

// Если мы хотим отредактировать другую часть документа с помощью конструктора,
// нам нужно будет подвести его курсор к узлу, который мы хотим редактировать.
builder.MoveToBookmark("MyBookmark");

// Перемещение его в закладку переместит его в первый узел в начальном и конечном узлах закладки, вложенный цикл.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// Мы также можем переместить курсор на отдельный узел следующим образом.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// Мы можем использовать специальные методы для перемещения к началу/концу документа.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### Смотрите также

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## MoveToBookmark(*string, bool, bool*) {#movetobookmark_1}

Перемещает курсор к закладке с большей точностью.

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | String | Имя закладки, на которую нужно переместить курсор. |
| isStart | Boolean | Когда`истинный` , перемещает курсор в начало закладки. Когда`ЛОЖЬ`, перемещает курсор в конец закладки. |
| isAfter | Boolean | Когда`истинный` , перемещает курсор после начальной или конечной позиции bookmark . Когда`ЛОЖЬ`, перемещает курсор до начальной или конечной позиции bookmark . |

### Возвращаемое значение

`истинный` если закладка была найдена;`ЛОЖЬ` в противном случае.

## Примечания

Перемещает курсор в позицию до или после начала или конца закладки.

Если желаемая позиция не находится на уровне строки, происходит переход к следующему абзацу.

Сравнение не учитывает регистр. Если закладка не найдена,`ЛОЖЬ` is возвращается, а курсор не перемещается.

## Примеры

Показывает, как переместить курсор точки вставки узла построителя документов на закладку.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Действительная закладка состоит из узла BookmarkStart, узла BookmarkEnd с
// соответствие имени закладки где-то позже и содержимому, заключенному в этих узлах.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// Существует 4 способа перемещения курсора конструктора документов к закладке.
// Если мы находимся между узлами BookmarkStart и BookmarkEnd, курсор будет внутри закладки.
// Это означает, что любой текст, добавленный конструктором, станет частью закладки.
// 1 - За пределами закладки, перед узлом BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, false));
builder.Write("1. ");

Assert.AreEqual("Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. Hello world!", doc.GetText().Trim());

// 2 - Внутри закладки, сразу после узла BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, true));
builder.Write("2. ");

Assert.AreEqual("2. Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world!", doc.GetText().Trim());

// 2 — Внутри закладки, прямо перед узлом BookmarkEnd:
Assert.True(builder.MoveToBookmark("MyBookmark", false, false));
builder.Write("3. ");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3.", doc.GetText().Trim());

// 4 - За пределами закладки, после узла BookmarkEnd:
Assert.True(builder.MoveToBookmark("MyBookmark", false, true));
builder.Write("4.");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3. 4.", doc.GetText().Trim());
```

### Смотрите также

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
