---
title: NodeCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words для .NET
description: Откройте для себя метод NodeCollection Add, который позволит вам легко добавлять узлы в свою коллекцию, упрощая и повышая эффективность управления данными.
type: docs
weight: 30
url: /ru/net/aspose.words/nodecollection/add/
---
## NodeCollection.Add method

Добавляет узел в конец коллекции.

```csharp
public void Add(Node node)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | Node | Узел, который будет добавлен в конец коллекции. |

### Исключения

| исключение | условие |
| --- | --- |
| NotSupportedException | The[`NodeCollection`](../) «глубокая» коллекция. |

## Примечания

Узел вставляется как дочерний элемент в объект узла, из которого была создана коллекция.

Если вставляемый узел был создан из другого документа, следует использовать [`ImportNode`](../../documentbase/importnode/) для импорта узла в текущий документ. Импортированный узел затем можно вставить в текущий документ.

## Примеры

Показывает, как подготовить новый узел раздела для редактирования.

```csharp
Document doc = new Document();

// Пустой документ содержит раздел, в котором есть тело, в котором, в свою очередь, есть абзац.
// Мы можем добавить содержимое в этот документ, добавив в этот абзац такие элементы, как текстовые строки, фигуры или таблицы.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Если мы добавим новый раздел, подобный этому, у него не будет тела или каких-либо других дочерних узлов.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Запустите метод «EnsureMinimum», чтобы добавить текст и абзац в этот раздел и начать его редактирование.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Смотрите также

* class [Node](../../node/)
* class [NodeCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
