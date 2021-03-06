---
title: ShapeRenderer
second_title: Справочник по API Aspose.Words для .NET
description: Предоставляет методы для рендеринга отдельногоShape../aspose.words.drawing/shape или жеGroupShape../aspose.words.drawing/groupshape в растровое или векторное изображение или в объект Graphics.
type: docs
weight: 4330
url: /ru/net/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class

Предоставляет методы для рендеринга отдельного[`Shape`](../../aspose.words.drawing/shape) или же[`GroupShape`](../../aspose.words.drawing/groupshape) в растровое или векторное изображение или в объект Graphics.

```csharp
public class ShapeRenderer : NodeRendererBase
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [ShapeRenderer](shaperenderer)(ShapeBase) | Инициализирует новый экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints) { get; } | Получает фактические границы фигуры в точках. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints) { get; } | Получает непрозрачные границы фигуры в точках. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints) { get; } | Получает фактический размер фигуры в точках. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels)(float, float) | Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels)(float, float, float) | Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels)(float, float) | Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels)(float, float, float) | Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels)(float, float) | Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels)(float, float, float) | Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale)(Graphics, float, float, float) | Преобразует форму вGraphics объект в указанном масштабе. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize)(Graphics, float, float, float, float) | Преобразует форму вGraphics объекта указанного размера. |
| [Save](../../aspose.words.rendering/noderendererbase/save)(Stream, ImageSaveOptions) | Преобразует форму в изображение и сохраняет в поток. |
| [Save](../../aspose.words.rendering/noderendererbase/save)(string, ImageSaveOptions) | Преобразует фигуру в изображение и сохраняет в файл. |

### Примеры

Показывает, как визуализировать фигуру с помощью объекта Graphics и отображать ее с помощью формы Windows.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    ShapeForm shapeForm = new ShapeForm(new Size(1017, 840));

    // Ниже приведены два способа использования класса «ShapeRenderer» для рендеринга фигуры в объект Graphics.
    // 1 - Создайте фигуру с диаграммой и визуализируйте ее в определенном масштабе.
    Chart chart = builder.InsertChart(ChartType.Pie, 500, 400).Chart;
    chart.Series.Clear();
    chart.Series.Add("Desktop Browser Market Share (Oct. 2020)",
        new[] { "Google Chrome", "Apple Safari", "Mozilla Firefox", "Microsoft Edge", "Other" },
        new[] { 70.33, 8.87, 7.69, 5.83, 7.28 });

    Shape chartShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    shapeForm.AddShapeToRenderToScale(chartShape, 0, 0, 1.5f);

    // 2 - Создайте группу фигур и визуализируйте ее до определенного размера.
    GroupShape group = new GroupShape(doc);
    group.Bounds = new RectangleF(0, 0, 100, 100);
    group.CoordSize = new Size(500, 500);

    Shape subShape = new Shape(doc, ShapeType.Rectangle);
    subShape.Width = 500;
    subShape.Height = 500;
    subShape.Left = 0;
    subShape.Top = 0;
    subShape.FillColor = Color.RoyalBlue;
    group.AppendChild(subShape);

    subShape = new Shape(doc, ShapeType.Image);
    subShape.Width = 450;
    subShape.Height = 450;
    subShape.Left = 25;
    subShape.Top = 25;
    subShape.ImageData.SetImage(ImageDir + "Logo.jpg");
    group.AppendChild(subShape);

    builder.InsertNode(group);

    GroupShape groupShape = (GroupShape)doc.GetChild(NodeType.GroupShape, 0, true);
    shapeForm.AddShapeToRenderToSize(groupShape, 880, 680, 100, 100);

    shapeForm.ShowDialog();
}

/// <summary>
/// Визуализирует и отображает список фигур.
/// </summary>
private class ShapeForm : Form
{
    public ShapeForm(Size size)
    {
        Size = size;
        mShapesToRender = new List<KeyValuePair<ShapeBase, float[]>>();
    }

    public void AddShapeToRenderToScale(ShapeBase shape, float x, float y, float scale)
    {
        mShapesToRender.Add(new KeyValuePair<ShapeBase, float[]>(shape, new[] {x, y, scale}));
    }

    public void AddShapeToRenderToSize(ShapeBase shape, float x, float y, float width, float height)
    {
        mShapesToRender.Add(new KeyValuePair<ShapeBase, float[]>(shape, new[] {x, y, width, height}));
    }

    protected override void OnPaint(PaintEventArgs e)
    {
        foreach (KeyValuePair<ShapeBase, float[]> renderingArgs in mShapesToRender)
            if (renderingArgs.Value.Length == 3)
                RenderShapeToScale(renderingArgs.Key, renderingArgs.Value[0], renderingArgs.Value[1],
                    renderingArgs.Value[2]);
            else if (renderingArgs.Value.Length == 4)
                RenderShapeToSize(renderingArgs.Key, renderingArgs.Value[0], renderingArgs.Value[1],
                    renderingArgs.Value[2], renderingArgs.Value[3]);
    }

    private void RenderShapeToScale(ShapeBase shape, float x, float y, float scale)
    {
        ShapeRenderer renderer = new ShapeRenderer(shape);
        using (Graphics formGraphics = CreateGraphics())
        {
            renderer.RenderToScale(formGraphics, x, y, scale);
        }
    }

    private void RenderShapeToSize(ShapeBase shape, float x, float y, float width, float height)
    {
        ShapeRenderer renderer = new ShapeRenderer(shape);
        using (Graphics formGraphics = CreateGraphics())
        {
            renderer.RenderToSize(formGraphics, x, y, width, height);
        }
    }

}
```

### Смотрите также

* class [NodeRendererBase](../noderendererbase)
* пространство имен [Aspose.Words.Rendering](../../aspose.words.rendering)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
