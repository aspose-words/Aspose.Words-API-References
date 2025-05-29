---
title: NodeRendererBase Class
linktitle: NodeRendererBase
articleTitle: NodeRendererBase
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Rendering.NodeRendererBase — основу для эффективного рендеринга Shape и OfficeMath при обработке документов.
type: docs
weight: 5280
url: /ru/net/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class

Базовый класс для[`ShapeRenderer`](../shaperenderer/) и[`OfficeMathRenderer`](../officemathrenderer/) .

Чтобы узнать больше, посетите[Работа с фигурами](https://docs.aspose.com/words/net/working-with-shapes/) документальная статья.

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
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels)(*float, float*) | Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels_1)(*float, float, float*) | Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels)(*float, float*) | Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels_1)(*float, float, float*) | Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels)(*float, float*) | Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels_1)(*float, float, float*) | Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(*Graphics, float, float, float*) | Отображает форму вGraphics объект в указанном масштабе. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(*Graphics, float, float, float, float*) | Отображает форму вGraphics объект указанного размера. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Визуализирует форму в изображение и сохраняет в поток. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_1)(*Stream, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Отображает форму в виде изображения SVG и сохраняет в потоке. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_2)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Преобразует форму в изображение и сохраняет в файл. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_3)(*string, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Визуализирует фигуру в изображение SVG и сохраняет в файл. |

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

* пространство имен [Aspose.Words.Rendering](../../aspose.words.rendering/)
* сборка [Aspose.Words](../../)
