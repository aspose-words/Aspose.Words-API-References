---
title: Node.Remove
second_title: Справочник по API Aspose.Words для .NET
description: Node метод. Удаляет себя от родителя.
type: docs
weight: 150
url: /ru/net/aspose.words/node/remove/
---
## Node.Remove method

Удаляет себя от родителя.

```csharp
public void Remove()
```

### Примеры

Показывает, как удалить все фигуры с изображениями из документа.

```csharp
Document doc = new Document(MyDir + "Images.docx");
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.OfType<Shape>().Count(s => s.HasImage));

foreach (Shape shape in shapes.OfType<Shape>())
    if (shape.HasImage) 
        shape.Remove();

Assert.AreEqual(0, shapes.OfType<Shape>().Count(s => s.HasImage));
```

Показывает, как удалить все дочерние узлы определенного типа из составного узла.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // Сохраняем следующий одноуровневый узел как переменную на случай, если мы захотим перейти к нему после удаления этого узла.
    Node nextNode = curNode.NextSibling;

    // Тело раздела может содержать узлы «Абзац» и «Таблица».
    // Если узел является таблицей, удалите его из родительского узла.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
```

### Смотрите также

* class [Node](../)
* пространство имен [Aspose.Words](../../node/)
* сборка [Aspose.Words](../../../)


