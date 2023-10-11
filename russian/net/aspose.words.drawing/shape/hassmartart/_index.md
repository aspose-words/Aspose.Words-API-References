---
title: Shape.HasSmartArt
second_title: Справочник по API Aspose.Words для .NET
description: Shape свойство. Возвращаетистинный если этоShape имеет объект SmartArt.
type: docs
weight: 90
url: /ru/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

Возвращает`истинный` если это[`Shape`](../) имеет объект SmartArt.

```csharp
public bool HasSmartArt { get; }
```

### Примеры

Показывает, как подсчитать количество фигур в документе с помощью объектов SmartArt.

```csharp
Document doc = new Document(MyDir + "SmartArt.docx");

int numberOfSmartArtShapes = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

Assert.AreEqual(2, numberOfSmartArtShapes);
```

### Смотрите также

* class [Shape](../)
* пространство имен [Aspose.Words.Drawing](../../shape/)
* сборка [Aspose.Words](../../../)


