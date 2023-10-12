---
title: Node.NextPreOrder
second_title: Справочник по API Aspose.Words для .NET
description: Node метод. Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного заказа.
type: docs
weight: 130
url: /ru/net/aspose.words/node/nextpreorder/
---
## Node.NextPreOrder method

Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного заказа.

```csharp
public Node NextPreOrder(Node rootNode)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| rootNode | Node | Верхний узел (предел) обхода. |

### Возвращаемое значение

Следующий узел в порядке предзаказа. Нуль, если достигнуто*rootNode*.

### Примеры

Показывает, как пройти по дереву узлов документа с помощью алгоритма обхода предварительного порядка и удалить любую встреченную фигуру с изображением.

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
* пространство имен [Aspose.Words](../../node/)
* сборка [Aspose.Words](../../../)


