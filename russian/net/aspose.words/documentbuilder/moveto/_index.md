---
title: DocumentBuilder.MoveTo
linktitle: MoveTo
articleTitle: MoveTo
second_title: Aspose.Words для .NET
description: Откройте для себя метод MoveTo в DocumentBuilder, позволяющий легко перемещаться по встроенным узлам и эффективно размещать курсор в концах абзацев для беспрепятственного редактирования документа.
type: docs
weight: 520
url: /ru/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

Перемещает курсор на встроенный узел или в конец абзаца.

```csharp
public void MoveTo(Node node)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | Node | Узел должен быть абзацем или прямым дочерним элементом абзаца. |

## Примечания

Когдаузел является узлом встроенного уровня, курсор перемещается на этот узел node , и последующее содержимое будет вставлено перед этим узлом.

Когдаузел это[`Paragraph`](../../paragraph/)курсор перемещается в конец абзаца , а дальнейшее содержимое вставляется непосредственно перед разрывом абзаца.

Когдаузел является узлом блочного уровня, но не[`Paragraph`](../../paragraph/), курсор перемещается в конец первого абзаца в узел уровня блока node , а последующий контент вставляется непосредственно перед разрывом абзаца.

## Примеры

Показывает, как переместить позицию курсора DocumentBuilder на указанный узел.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Конструктор документов имеет курсор, который действует как часть документа
// где конструктор добавляет новые узлы, когда мы используем его методы построения документа.
// Этот курсор функционирует так же, как мигающий курсор Microsoft Word,
// и он также всегда оказывается сразу после любого узла, который только что вставил строитель.
// Чтобы добавить содержимое в другую часть документа,
// мы можем переместить курсор на другой узел с помощью метода «MoveTo».
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// Курсор теперь находится перед узлом, в который мы его переместили.
// Добавление второго запуска вставит его перед первым запуском.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Переместите курсор в конец документа, чтобы продолжить добавление текста в конец, как и раньше.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

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
