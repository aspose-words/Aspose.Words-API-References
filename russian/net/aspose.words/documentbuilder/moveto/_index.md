---
title: DocumentBuilder.MoveTo
linktitle: MoveTo
articleTitle: MoveTo
second_title: Aspose.Words для .NET
description: DocumentBuilder MoveTo метод. Перемещает курсор к строчному узлу или в конец абзаца на С#.
type: docs
weight: 480
url: /ru/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

Перемещает курсор к строчному узлу или в конец абзаца.

```csharp
public void MoveTo(Node node)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | Node | Узел должен быть абзацем или прямым дочерним элементом абзаца. |

## Примечания

Когдаузел является узлом встроенного уровня, курсор перемещается на этот узел node , и дальнейшее содержимое будет вставлено перед этим узлом.

Когдаузел это[`Paragraph`](../../paragraph/), курсор перемещается в конец параграфа , и дальнейшее содержимое будет вставлено непосредственно перед разрывом абзаца.

Когдаузел является узлом блочного уровня, но не[`Paragraph`](../../paragraph/), курсор перемещается в конец первого абзаца в node уровня блока, и дальнейшее содержимое будет вставлено непосредственно перед разрывом абзаца.

## Примеры

Показывает, как переместить позицию курсора DocumentBuilder в указанный узел.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// В конструкторе документов есть курсор, который действует как часть документа
// где построитель добавляет новые узлы, когда мы используем его методы построения документа.
// Этот курсор работает так же, как мигающий курсор Microsoft Word,
// и он также всегда заканчивается сразу после любого узла, который только что вставил построитель.
// Чтобы добавить контент в другую часть документа,
// мы можем переместить курсор в другой узел с помощью метода «MoveTo».
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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
