---
title: DocumentBuilder.IsAtStartOfParagraph
linktitle: IsAtStartOfParagraph
articleTitle: IsAtStartOfParagraph
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IsAtStartOfParagraph DocumentBuilder. Легко проверяйте, находится ли курсор в начале абзаца, для эффективного редактирования текста.
type: docs
weight: 130
url: /ru/net/aspose.words/documentbuilder/isatstartofparagraph/
---
## DocumentBuilder.IsAtStartOfParagraph property

Возврат`истинный`если курсор находится в начале текущего абзаца (перед курсором нет текста).

```csharp
public bool IsAtStartOfParagraph { get; }
```

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
