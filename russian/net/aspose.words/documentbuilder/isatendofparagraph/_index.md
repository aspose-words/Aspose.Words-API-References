---
title: DocumentBuilder.IsAtEndOfParagraph
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder свойство. Возвращает true если курсор находится в конце текущего абзаца.
type: docs
weight: 100
url: /ru/net/aspose.words/documentbuilder/isatendofparagraph/
---
## DocumentBuilder.IsAtEndOfParagraph property

Возвращает true, если курсор находится в конце текущего абзаца.

```csharp
public bool IsAtEndOfParagraph { get; }
```

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

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


