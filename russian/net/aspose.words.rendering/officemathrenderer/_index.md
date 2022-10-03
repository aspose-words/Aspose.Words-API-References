---
title: OfficeMathRenderer
second_title: Справочник по API Aspose.Words для .NET
description: Предоставляет методы для рендеринга отдельногоOfficeMath../aspose.words.math/officemath/ в растровое или векторное изображение или в объект Graphics.
type: docs
weight: 4300
url: /ru/net/aspose.words.rendering/officemathrenderer/
---
## OfficeMathRenderer class

Предоставляет методы для рендеринга отдельного[`OfficeMath`](../../aspose.words.math/officemath/) в растровое или векторное изображение или в объект Graphics.

```csharp
public class OfficeMathRenderer : NodeRendererBase
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [OfficeMathRenderer](officemathrenderer/)(OfficeMath) | Инициализирует новый экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | Получает фактические границы фигуры в точках. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | Получает непрозрачные границы фигуры в точках. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | Получает фактический размер фигуры в точках. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(float, float) | Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(float, float, float) | Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(float, float) | Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(float, float, float) | Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(float, float) | Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(float, float, float) | Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(Graphics, float, float, float) | Преобразует форму вGraphics объект в указанном масштабе. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(Graphics, float, float, float, float) | Преобразует форму вGraphics объекта указанного размера. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(Stream, ImageSaveOptions) | Преобразует форму в изображение и сохраняет в поток. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(string, ImageSaveOptions) | Преобразует фигуру в изображение и сохраняет в файл. |

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

* class [NodeRendererBase](../noderendererbase/)
* пространство имен [Aspose.Words.Rendering](../../aspose.words.rendering/)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
