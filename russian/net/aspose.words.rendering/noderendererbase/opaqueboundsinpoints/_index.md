---
title: NodeRendererBase.OpaqueBoundsInPoints
linktitle: OpaqueBoundsInPoints
articleTitle: OpaqueBoundsInPoints
second_title: Aspose.Words для .NET
description: Откройте для себя свойство NodeRendererBase OpaqueBoundsInPoints, которое позволяет легко получать доступ к границам фигур в точках, повышая точность и эффективность вашего дизайна.
type: docs
weight: 20
url: /ru/net/aspose.words.rendering/noderendererbase/opaqueboundsinpoints/
---
## NodeRendererBase.OpaqueBoundsInPoints property

Получает непрозрачные границы фигуры в точках.

```csharp
public RectangleF OpaqueBoundsInPoints { get; }
```

## Примечания

Это свойство возвращает непрозрачный (т.е. прозрачные части фигуры игнорируются) ограничивающий прямоугольник фигуры. Границы учитывают поворот фигуры.

## Примеры

Показывает, как измерять и масштабировать фигуры.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Проверяем размер изображения, которое объект OfficeMath создаст при его рендеринге.
Assert.AreEqual(122.0f, renderer.SizeInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.15f);

Assert.AreEqual(122.0f, renderer.BoundsInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.15f);

// Фигуры с прозрачными частями могут содержать разные значения в свойствах «OpaqueBoundsInPoints».
Assert.AreEqual(122.0f, renderer.OpaqueBoundsInPoints.Width, 0.25f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Получить размер фигуры в пикселях с линейным масштабированием до определенного DPI.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Получить размер фигуры в пикселях, но с разным DPI для горизонтальных и вертикальных размеров.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(27, bounds.Height);

// Непрозрачные границы здесь также могут различаться.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(19, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(29, bounds.Height);
```

### Смотрите также

* class [NodeRendererBase](../)
* пространство имен [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* сборка [Aspose.Words](../../../)
