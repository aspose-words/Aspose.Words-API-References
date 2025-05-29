---
title: Node.CustomNodeId
linktitle: CustomNodeId
articleTitle: CustomNodeId
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Node CustomNodeId для эффективной идентификации пользовательских узлов. Улучшите свой проект с помощью уникальных идентификаторов для лучшей организации!
type: docs
weight: 10
url: /ru/net/aspose.words/node/customnodeid/
---
## Node.CustomNodeId property

Указывает пользовательский идентификатор узла.

```csharp
public int CustomNodeId { get; set; }
```

## Примечания

По умолчанию — ноль.

Этот идентификатор можно задать и использовать произвольно. Например, как ключ для получения внешних данных.

Важное примечание: указанное значение не сохраняется в выходном файле и существует только в течение срока службы узла.

## Примеры

Показывает, как проходить по коллекции дочерних узлов составного узла.

```csharp
Document doc = new Document();

// Добавьте две трассы и одну форму в качестве дочерних узлов в первый абзац этого документа.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Обратите внимание, что «CustomNodeId» не сохраняется в выходном файле и существует только в течение срока службы узла.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Проходим по коллекции непосредственных дочерних элементов абзаца,
// и распечатать любые найденные нами фрагменты или формы.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
```

### Смотрите также

* class [Node](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
