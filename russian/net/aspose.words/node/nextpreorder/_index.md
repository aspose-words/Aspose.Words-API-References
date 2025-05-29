---
title: Node.NextPreOrder
linktitle: NextPreOrder
articleTitle: NextPreOrder
second_title: Aspose.Words для .NET
description: Откройте для себя метод Node NextPreOrder для эффективного обхода дерева. Узнайте, как эффективно извлекать следующий узел с помощью алгоритма предварительного порядка!
type: docs
weight: 130
url: /ru/net/aspose.words/node/nextpreorder/
---
## Node.NextPreOrder method

Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка.

```csharp
public Node NextPreOrder(Node rootNode)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| rootNode | Node | Верхний узел (предел) обхода. |

### Возвращаемое значение

Следующий узел в порядке предварительного порядка. Null, если достигнут*rootNode*.

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
