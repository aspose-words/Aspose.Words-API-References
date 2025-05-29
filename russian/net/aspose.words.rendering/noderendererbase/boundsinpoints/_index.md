---
title: NodeRendererBase.BoundsInPoints
linktitle: BoundsInPoints
articleTitle: BoundsInPoints
second_title: Aspose.Words для .NET
description: Откройте для себя свойство NodeRendererBase BoundsInPoints для доступа к точным размерам фигур в точках, что повысит точность и эффективность вашего проекта.
type: docs
weight: 10
url: /ru/net/aspose.words.rendering/noderendererbase/boundsinpoints/
---
## NodeRendererBase.BoundsInPoints property

Получает фактические границы фигуры в точках.

```csharp
public RectangleF BoundsInPoints { get; }
```

## Примечания

Это свойство возвращает фактический (отображенный на странице) ограничивающий прямоугольник фигуры. Границы учитывают поворот фигуры (если таковой имеется).

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
