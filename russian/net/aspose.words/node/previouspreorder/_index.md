---
title: Node.PreviousPreOrder
linktitle: PreviousPreOrder
articleTitle: PreviousPreOrder
second_title: Aspose.Words для .NET
description: Откройте для себя метод Node PreviousPreOrder для эффективного извлечения предыдущего узла с использованием алгоритма обхода дерева предварительного порядка для оптимизированной обработки данных.
type: docs
weight: 140
url: /ru/net/aspose.words/node/previouspreorder/
---
## Node.PreviousPreOrder method

Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка.

```csharp
public Node PreviousPreOrder(Node rootNode)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| rootNode | Node | Верхний узел (предел) обхода. |

### Возвращаемое значение

Предыдущий узел в порядке предварительного порядка. Нуль, если достигнут*rootNode*.

## Примеры

Показывает, как обойти дерево узлов документа, используя алгоритм обхода в предварительном порядке, и удалить любую встреченную фигуру с изображением.

```csharp
Document doc = new Document(MyDir + "Images.docx");

Assert.AreEqual(9, 
    doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().Count(s => s.HasImage));

Node curNode = doc;
while (curNode != null)
{
    Node nextNode = curNode.NextPreOrder(doc);

    if (curNode.PreviousPreOrder(doc) != null && nextNode != null)
        Assert.AreEqual(curNode, nextNode.PreviousPreOrder(doc));

    if (curNode.NodeType == NodeType.Shape && ((Shape)curNode).HasImage)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0,
    doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().Count(s => s.HasImage));
```

### Смотрите также

* class [Node](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
