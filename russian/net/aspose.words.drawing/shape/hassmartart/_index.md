---
title: Shape.HasSmartArt
linktitle: HasSmartArt
articleTitle: HasSmartArt
second_title: Aspose.Words для .NET
description: Узнайте, содержит ли ваша форма объект SmartArt со свойством HasSmartArt. Откройте для себя творческие возможности дизайна для ваших проектов!
type: docs
weight: 100
url: /ru/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

Возврат`истинный` если это[`Shape`](../) имеет объект SmartArt.

```csharp
public bool HasSmartArt { get; }
```

## Примеры

Показывает, как подсчитать количество фигур в документе с помощью объектов SmartArt.

```csharp
Document doc = new Document(MyDir + "SmartArt.docx");

int numberOfSmartArtShapes = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

Assert.AreEqual(2, numberOfSmartArtShapes);
```

### Смотрите также

* class [Shape](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
