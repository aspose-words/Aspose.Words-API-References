---
title: NodeCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: NodeCollection Item свойство. Извлекает узел по заданному индексу на С#.
type: docs
weight: 20
url: /ru/net/aspose.words/nodecollection/item/
---
## NodeCollection indexer

Извлекает узел по заданному индексу.

```csharp
public Node this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Индекс коллекции узлов. |

## Примечания

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ из задней части коллекции. Например, -1 означает последний элемент, -2 означает предпоследний элемент и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается нулевая ссылка.

Если индекс отрицателен и его абсолютное значение превышает количество элементов в списке, возвращается нулевая ссылка.

## Примеры

Показывает, как перемещаться по коллекции дочерних узлов составного узла.

```csharp
Document doc = new Document();

// Добавьте два прогона и одну фигуру в качестве дочерних узлов в первый абзац этого документа.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Обратите внимание, что CustomNodeId не сохраняется в выходном файле и существует только во время существования узла.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Перебираем коллекцию непосредственных дочерних элементов абзаца,
// и распечатываем любые фрагменты или фигуры, которые мы находим внутри.
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

* class [Node](../../node/)
* class [NodeCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
