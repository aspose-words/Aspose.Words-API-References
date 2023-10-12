---
title: NodeRendererBase.BoundsInPoints
second_title: Справочник по API Aspose.Words для .NET
description: NodeRendererBase свойство. Получает фактические границы фигуры в точках.
type: docs
weight: 10
url: /ru/net/aspose.words.rendering/noderendererbase/boundsinpoints/
---
## NodeRendererBase.BoundsInPoints property

Получает фактические границы фигуры в точках.

```csharp
public RectangleF BoundsInPoints { get; }
```

### Примечания

Это свойство возвращает фактическую (отрисованную на странице) ограничивающую рамку фигуры. Границы учитывают вращение фигуры (если таковое имеется).

### Примеры

Показывает, как измерять и масштабировать фигуры.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Проверяем размер изображения, которое объект OfficeMath создаст при его рендеринге.
Assert.AreEqual(119.0f, renderer.SizeInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.1f);

Assert.AreEqual(119.0f, renderer.BoundsInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.1f);

// Фигуры с прозрачными частями могут содержать разные значения в свойствах OpaqueBoundsInPoints.
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Получаем размер фигуры в пикселях с линейным масштабированием до определенного разрешения.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Получаем размер фигуры в пикселях, но с разным DPI для горизонтального и вертикального размеров.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(28, bounds.Height);

// Здесь также непрозрачные границы могут различаться.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(30, bounds.Height);
```

### Смотрите также

* class [NodeRendererBase](../)
* пространство имен [Aspose.Words.Rendering](../../noderendererbase/)
* сборка [Aspose.Words](../../../)


