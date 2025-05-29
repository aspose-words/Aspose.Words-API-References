---
title: NodeRendererBase.GetOpaqueBoundsInPixels
linktitle: GetOpaqueBoundsInPixels
articleTitle: GetOpaqueBoundsInPixels
second_title: Aspose.Words для .NET
description: Узнайте, как метод NodeRendererBase GetOpaqueBoundsInPixels эффективно вычисляет границы фигуры в пикселях, оптимизируя масштаб и разрешение.
type: docs
weight: 50
url: /ru/net/aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/
---
## GetOpaqueBoundsInPixels(*float, float*) {#getopaqueboundsinpixels}

Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения.

```csharp
public Rectangle GetOpaqueBoundsInPixels(float scale, float dpi)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| scale | Single | Коэффициент масштабирования (1,0 = 100%). |
| dpi | Single | Разрешение для преобразования точек в пиксели (точек на дюйм). |

### Возвращаемое значение

Непрозрачный прямоугольник фигуры в пикселях.

## Примечания

Этот метод преобразует[`OpaqueBoundsInPoints`](../opaqueboundsinpoints/) в прямоугольник в пикселях и полезен , когда вы хотите создать растровое изображение для визуализации фигуры, в которой непрозрачной является только часть фигуры.

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

---

## GetOpaqueBoundsInPixels(*float, float, float*) {#getopaqueboundsinpixels_1}

Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения.

```csharp
public Rectangle GetOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| scale | Single | Коэффициент масштабирования (1,0 = 100%). |
| horizontalDpi | Single | Горизонтальное разрешение для преобразования из точек в пиксели (точек на дюйм). |
| verticalDpi | Single | Вертикальное разрешение для преобразования из точек в пиксели (точек на дюйм). |

### Возвращаемое значение

Непрозрачный прямоугольник фигуры в пикселях.

## Примечания

Этот метод преобразует[`OpaqueBoundsInPoints`](../opaqueboundsinpoints/) в прямоугольник в пикселях и полезен , когда вы хотите создать растровое изображение для визуализации фигуры, в которой непрозрачной является только часть фигуры.

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
