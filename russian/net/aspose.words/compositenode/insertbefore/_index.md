---
title: CompositeNode.InsertBefore
second_title: Справочник по API Aspose.Words для .NET
description: CompositeNode метод. Вставляет указанный узел непосредственно перед указанным ссылочным узлом.
type: docs
weight: 150
url: /ru/net/aspose.words/compositenode/insertbefore/
---
## CompositeNode.InsertBefore method

Вставляет указанный узел непосредственно перед указанным ссылочным узлом.

```csharp
public Node InsertBefore(Node newChild, Node refChild)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| newChild | Node | Узел для вставки. |
| refChild | Node | Узел, который является эталонным узлом. Новый дочерний элемент помещается перед этим узлом. |

### Возвращаемое значение

Вставленный узел.

### Примечания

Если refChild имеет значение null, вставляет newChild в конец списка дочерних узлов.

Если новый дочерний элемент уже находится в дереве, он сначала удаляется.

Если вставляемый узел был создан из другого документа, следует использовать [`ImportNode`](../../documentbase/importnode/) чтобы импортировать узел в текущий документ. Затем импортированный узел можно вставить в текущий документ.

### Примеры

Показывает, как добавлять, обновлять и удалять дочерние узлы в коллекции дочерних узлов CompositeNode.

```csharp
Document doc = new Document();

// Пустой документ по умолчанию имеет один абзац.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Составные узлы, такие как наш абзац, могут содержать другие составные и встроенные узлы в качестве дочерних элементов.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Создадим еще три узла запуска.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Тело документа не будет отображать эти прогоны, пока мы не вставим их в составной узел
// это само по себе является частью дерева узлов документа, как мы сделали при первом запуске.
// Мы можем определить, где находится текстовое содержимое узлов, которые мы вставляем
// появляется в документе путем указания места вставки относительно другого узла в абзаце.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Вставляем второй прогон в абзац перед начальным прогоном.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Вставляем третий прогон после первого прогона.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Вставляем первую строку в начало коллекции дочерних узлов абзаца.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Мы можем изменить содержимое прогона, отредактировав и удалив существующие дочерние узлы.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Смотрите также

* class [Node](../../node/)
* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../compositenode/)
* сборка [Aspose.Words](../../../)


