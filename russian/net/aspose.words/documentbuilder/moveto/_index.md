---
title: DocumentBuilder.MoveTo
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder метод. Перемещает курсор на встроенный узел или в конец абзаца.
type: docs
weight: 460
url: /ru/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

Перемещает курсор на встроенный узел или в конец абзаца.

```csharp
public void MoveTo(Node node)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | Node | Узел должен быть абзацем или прямым потомком абзаца. |

### Примечания

Когдаузел является узлом встроенного уровня, курсор перемещается на этот node , и перед этим узлом будет вставлено дополнительное содержимое.

Когдаузел это **Параграф**, курсор перемещается в конец абзаца , и дальнейшее содержимое будет вставлено непосредственно перед разрывом абзаца.

Когдаузелявляется блочным узлом, но не абзацем, курсор перемещается в конец первого абзаца в блочный узел node , и дальнейшее содержимое будет вставлено непосредственно перед разрывом абзаца.

### Примеры

Показывает, как переместить позицию курсора DocumentBuilder в указанный узел.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// В построителе документа есть курсор, который действует как часть документа
// где построитель добавляет новые узлы, когда мы используем его методы построения документа.
// Этот курсор действует так же, как мигающий курсор Microsoft Word,
// и он также всегда заканчивается сразу после любого узла, который только что вставил строитель.
// Чтобы добавить содержимое в другую часть документа,
// мы можем переместить курсор на другой узел с помощью метода "MoveTo".
// Курсор теперь перед узлом, на который мы его переместили.
// Добавление второго запуска вставит его перед первым запуском.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Переместите курсор в конец документа, чтобы продолжить добавление текста в конец, как и раньше.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


