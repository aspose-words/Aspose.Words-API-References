---
title: MoveToBookmark
second_title: Справочник по API Aspose.Words для .NET
description: Перемещает курсор на закладку.
type: docs
weight: 470
url: /ru/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(string) {#movetobookmark}

Перемещает курсор на закладку.

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | String | Имя закладки, на которую нужно переместить курсор. |

### Возвращаемое значение

Истинно, если закладка найдена; ложно в противном случае.

### Примечания

Перемещает курсор в позицию сразу после начала закладки с указанным именем .

Сравнение не чувствительно к регистру. Если закладка не найдена, возвращается false is и курсор не перемещается.

Вставка нового текста не заменяет существующий текст закладки.

Обратите внимание, что некоторые закладки в документе назначены полям формы. Переход на такую закладку и вставка туда текста вставляет текст в код поля формы . Хотя это не сделает поле формы недействительным, текст insert не будет виден, поскольку он становится частью кода поля.

### Примеры

Показывает, как перемещать курсор конструктора документов в разные узлы документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создать допустимую закладку, объект, состоящий из узлов, заключенных в начальный узел закладки,
 // и конечный узел закладки.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.ChildNodes;

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Курсор построителя документа всегда находится перед узлом, который мы добавили последним.
// Если курсор построителя находится в конце документа, его текущий узел будет нулевым.
// Предыдущий узел — это последний добавленный нами конечный узел закладки.
// Добавление новых узлов с помощью построителя добавит их к последнему узлу.
Assert.Null(builder.CurrentNode);

// Если мы хотим отредактировать другую часть документа с помощью конструктора,
// нам нужно будет подвести его курсор к узлу, который мы хотим отредактировать.
builder.MoveToBookmark("MyBookmark");

// Перемещение его в закладку переместит его в первый узел в пределах начального и конечного узлов закладки, замкнутого цикла.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// Мы также можем переместить курсор на отдельный узел вот так.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// Мы можем использовать специальные методы для перехода к началу/концу документа.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### Смотрите также

* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

---

## MoveToBookmark(string, bool, bool) {#movetobookmark_1}

Перемещает курсор к закладке с большей точностью.

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | String | Имя закладки, на которую нужно переместить курсор. |
| isStart | Boolean | При значении true курсор перемещается в начало закладки. При значении false курсор перемещается в конец закладки. |
| isAfter | Boolean | При значении true курсор перемещается после начальной или конечной позиции bookmark . При значении false курсор перемещается перед начальной или конечной позицией bookmark . |

### Возвращаемое значение

Истинно, если закладка найдена; ложно в противном случае.

### Примечания

Перемещает курсор в положение до или после начала или конца закладки.

Если нужная позиция не на встроенном уровне, выполняется переход к следующему абзацу.

Сравнение не чувствительно к регистру. Если закладка не найдена, возвращается false is и курсор не перемещается.

### Примеры

Показывает, как переместить курсор точки вставки узла компоновщика документов на закладку.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Действительная закладка состоит из узла BookmarkStart, узла BookmarkEnd с
// сопоставление имени закладки где-то позже и содержимого, заключенного в этих узлах.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// Существует 4 способа перемещения курсора конструктора документов на закладку.
// Если мы находимся между узлами BookmarkStart и BookmarkEnd, то курсор будет внутри закладки.
// Это означает, что любой текст, добавленный конструктором, станет частью закладки.
// 1 - Снаружи закладки, перед узлом BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, false));
builder.Write("1. ");

Assert.AreEqual("Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. Hello world!", doc.GetText().Trim());

// 2 - Внутри закладки, сразу после узла BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, true));
builder.Write("2. ");

Assert.AreEqual("2. Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world!", doc.GetText().Trim());

// 2 - Внутри закладки, прямо перед узлом BookmarkEnd:
Assert.True(builder.MoveToBookmark("MyBookmark", false, false));
builder.Write("3. ");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3.", doc.GetText().Trim());

// 4 - Вне закладки, после узла BookmarkEnd:
Assert.True(builder.MoveToBookmark("MyBookmark", false, true));
builder.Write("4.");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3. 4.", doc.GetText().Trim());
```

### Смотрите также

* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
