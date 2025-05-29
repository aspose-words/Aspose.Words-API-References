---
title: Document.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words для .NET
description: Узнайте, как использовать метод EnsureMinimum для автоматического создания разделов и абзацев в документах, обеспечивая полноту и организованность контента.
type: docs
weight: 620
url: /ru/net/aspose.words/document/ensureminimum/
---
## Document.EnsureMinimum method

Если документ не содержит разделов, создает один раздел с одним абзацем.

```csharp
public void EnsureMinimum()
```

## Примеры

Показывает, как обеспечить наличие в документе минимального набора узлов, необходимого для редактирования его содержимого.

```csharp
// Вновь созданный документ содержит один дочерний раздел, который включает в себя один дочерний текст и один дочерний абзац.
// Мы можем редактировать содержимое тела документа, добавляя в этот абзац такие узлы, как Runs или встроенные Shapes.
Document doc = new Document();
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(doc, nodes[0].ParentNode);

Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(nodes[0], nodes[1].ParentNode);

Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);
Assert.AreEqual(nodes[1], nodes[2].ParentNode);

// Это минимальный набор узлов, который нам нужен для редактирования документа.
// Если мы удалим любой из них, мы больше не сможем редактировать документ.
doc.RemoveAllChildren();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);

// Вызовите этот метод, чтобы убедиться, что документ содержит по крайней мере эти три узла, чтобы мы могли редактировать его снова.
doc.EnsureMinimum();

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);

((Paragraph)nodes[2]).Runs.Add(new Run(doc, "Hello world!"));
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
