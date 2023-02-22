---
title: Class NodeRendererBase
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Rendering.NodeRendererBase сорт. Базовый класс дляShapeRenderer а такжеOfficeMathRenderer .
type: docs
weight: 4290
url: /ru/net/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class

Базовый класс для[`ShapeRenderer`](../shaperenderer/) а также[`OfficeMathRenderer`](../officemathrenderer/) .

```csharp
public abstract class NodeRendererBase
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | Получает фактические границы фигуры в точках. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | Получает непрозрачные границы фигуры в точках. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | Получает фактический размер фигуры в точках. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels)(float, float) | Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels_1)(float, float, float) | Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels)(float, float) | Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels_1)(float, float, float) | Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels)(float, float) | Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels_1)(float, float, float) | Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(Graphics, float, float, float) | Преобразует форму вGraphics объект в указанном масштабе. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(Graphics, float, float, float, float) | Преобразует форму вGraphics объекта указанного размера. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save)(Stream, ImageSaveOptions) | Преобразует форму в изображение и сохраняет в поток. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_1)(string, ImageSaveOptions) | Преобразует фигуру в изображение и сохраняет в файл. |

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

// Формы с прозрачными частями могут содержать разные значения в свойствах "OpaqueBoundsInPoints".
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Получить размер фигуры в пикселях с линейным масштабированием до определенного DPI.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Получаем размер фигуры в пикселях, но с разным DPI для горизонтального и вертикального размеров.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(28, bounds.Height);

// Непрозрачные границы здесь тоже могут быть разными.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(30, bounds.Height);
```

### Смотрите также

* пространство имен [Aspose.Words.Rendering](../../aspose.words.rendering/)
* сборка [Aspose.Words](../../)


