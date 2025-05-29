---
title: DocumentBuilder.MoveToBookmark
linktitle: MoveToBookmark
articleTitle: MoveToBookmark
second_title: Aspose.Words для .NET
description: Легко перемещайтесь по документам с помощью метода MoveToBookmark в DocumentBuilder, мгновенно устанавливая курсор на любую закладку для расширенного редактирования.
type: docs
weight: 530
url: /ru/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(*string*) {#movetobookmark}

Перемещает курсор на закладку.

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | String | Имя закладки, на которую следует переместить курсор. |

### Возвращаемое значение

`истинный` если закладка найдена;`ЛОЖЬ` в противном случае.

## Примечания

Перемещает курсор в позицию сразу после начала закладки с указанным именем the .

Сравнение не чувствительно к регистру. Если закладка не найдена,`ЛОЖЬ` is возвращается, а курсор не перемещается.

Вставка нового текста не заменяет существующий текст закладки.

Обратите внимание, что некоторые закладки в документе назначены полям формы. Переход к такой закладке и вставка текста туда вставляет текст в код поля формы . Хотя это не сделает поле формы недействительным, текст вставленный не будет виден, поскольку он становится частью кода поля.

## Примеры

Показывает, как перемещать курсор конструктора документов на различные узлы документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создать действительную закладку, сущность, состоящую из узлов, заключенных в начальный узел закладки,
 // и конечный узел закладки.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Курсор конструктора документов всегда находится впереди узла, который мы добавили с его помощью в последний раз.
// Если курсор конструктора находится в конце документа, его текущий узел будет нулевым.
// Предыдущий узел — это конечный узел закладки, который мы добавили последним.
// Добавление новых узлов с помощью конструктора добавит их к последнему узлу.
Assert.Null(builder.CurrentNode);

// Если мы хотим отредактировать другую часть документа с помощью конструктора,
// нам нужно будет подвести курсор к узлу, который мы хотим редактировать.
builder.MoveToBookmark("MyBookmark");

// Перемещение его в закладку переместит его в первый узел в пределах начального и конечного узлов закладки, заключенного в закладку.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// Мы также можем переместить курсор на отдельный узел следующим образом.
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

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## MoveToBookmark(*string, bool, bool*) {#movetobookmark_1}

Перемещает курсор на закладку с большей точностью.

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | String | Имя закладки, на которую следует переместить курсор. |
| isStart | Boolean | Когда`истинный` , перемещает курсор в начало закладки. Когда`ЛОЖЬ`, перемещает курсор в конец закладки. |
| isAfter | Boolean | Когда`истинный` , перемещает курсор в положение после закладки start или end. Когда`ЛОЖЬ`перемещает курсор в положение перед начальной или конечной позицией bookmark . |

### Возвращаемое значение

`истинный` если закладка найдена;`ЛОЖЬ` в противном случае.

## Примечания

Перемещает курсор в позицию до или после начала или конца закладки.

Если требуемая позиция не находится на уровне строки, выполняется переход к следующему абзацу.

Сравнение не чувствительно к регистру. Если закладка не найдена,`ЛОЖЬ` is возвращается, а курсор не перемещается.

## Примеры

Показывает, как переместить курсор точки вставки узла конструктора документов на закладку.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Действительная закладка состоит из узла BookmarkStart, узла BookmarkEnd с
// соответствующее имя закладки где-то далее и содержимое, заключенное в этих узлах.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// Существует 4 способа перемещения курсора конструктора документов на закладку.
// Если мы находимся между узлами BookmarkStart и BookmarkEnd, курсор будет внутри закладки.
// Это означает, что любой текст, добавленный конструктором, станет частью закладки.
// 1 — Снаружи закладки, перед узлом BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, false));
builder.Write("1. ");

Assert.AreEqual("Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. Hello world!", doc.GetText().Trim());

// 2 — Внутри закладки, сразу после узла BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, true));
builder.Write("2. ");

Assert.AreEqual("2. Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world!", doc.GetText().Trim());

// 2 — Внутри закладки, прямо перед узлом BookmarkEnd:
Assert.True(builder.MoveToBookmark("MyBookmark", false, false));
builder.Write("3. ");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3.", doc.GetText().Trim());

// 4 — За пределами закладки, после узла BookmarkEnd:
Assert.True(builder.MoveToBookmark("MyBookmark", false, true));
builder.Write("4.");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3. 4.", doc.GetText().Trim());
```

### Смотрите также

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
