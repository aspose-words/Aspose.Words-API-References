---
title: SoftEdgeFormat.Radius
linktitle: Radius
articleTitle: Radius
second_title: Aspose.Words для .NET
description: Откройте для себя свойство SoftEdgeFormat Radius для легкой настройки эффектов смягчения краев. Управляйте длиной радиуса с точностью для потрясающих визуальных результатов.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing/softedgeformat/radius/
---
## SoftEdgeFormat.Radius property

Возвращает или задает двойное значение, представляющее длину радиуса для эффекта мягкого края в пунктах (pt). Значение по умолчанию — 0.0.

```csharp
public double Radius { get; set; }
```

## Примеры

Показывает, как установить ограничение на разрешение изображения.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

Показывает, как работать с форматированием с мягкими краями.

```csharp
DocumentBuilder builder = new DocumentBuilder();
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 200);

// Применить мягкие края к фигуре.
shape.SoftEdge.Radius = 30;

builder.Document.Save(ArtifactsDir + "Shape.SoftEdge.docx");

// Загрузить документ с прямоугольной формой и мягкими краями.
Document doc = new Document(ArtifactsDir + "Shape.SoftEdge.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
SoftEdgeFormat softEdgeFormat = shape.SoftEdge;

// Проверьте радиус скругления кромок.
Assert.AreEqual(30, softEdgeFormat.Radius);

// Удалить мягкие края из фигуры.
softEdgeFormat.Remove();

// Проверьте радиус удаленного мягкого края.
Assert.AreEqual(0, softEdgeFormat.Radius);
```

### Смотрите также

* class [SoftEdgeFormat](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
