---
title: DocumentBuilder.CurrentNode
linktitle: CurrentNode
articleTitle: CurrentNode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CurrentNode в DocumentBuilder, чтобы легко получить доступ к выбранному узлу, повысив эффективность редактирования документов и рабочий процесс.
type: docs
weight: 40
url: /ru/net/aspose.words/documentbuilder/currentnode/
---
## DocumentBuilder.CurrentNode property

Получает узел, который в данный момент выбран в этом DocumentBuilder.

```csharp
public Node CurrentNode { get; }
```

## Примечания

`CurrentNode` это курсор[`DocumentBuilder`](../) и указывает на[`Node`](../../node/) , который является прямым потомком[`Paragraph`](../../paragraph/) . Любые операции вставки, которые вы выполняете с помощью [`DocumentBuilder`](../) вставлю перед`CurrentNode`.

Если текущий абзац пуст или курсор расположен just перед концом абзаца или структурированного тега документа,`CurrentNode` возвращается`нулевой`.

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
