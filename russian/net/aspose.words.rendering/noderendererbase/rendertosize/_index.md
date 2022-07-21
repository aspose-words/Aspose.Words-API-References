---
title: RenderToSize
second_title: Справочник по API Aspose.Words для .NET
description: Преобразует форму вGraphics объекта указанного размера.
type: docs
weight: 80
url: /ru/net/aspose.words.rendering/noderendererbase/rendertosize/
---
## NodeRendererBase.RenderToSize method

Преобразует форму вGraphics объекта указанного размера.

```csharp
public float RenderToSize(Graphics graphics, float x, float y, float width, float height)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| graphics | Graphics | Объект, на который выполняется рендеринг. |
| x | Single | Координата X (в мировых единицах измерения) верхнего левого угла отображаемой фигуры. |
| y | Single | Координата Y (в мировых единицах измерения) верхнего левого угла отображаемой фигуры. |
| width | Single | Максимальная ширина (в мировых единицах), которую может занимать отображаемая фигура. |
| height | Single | Максимальная высота (в мировых единицах), которую может занимать отображаемая фигура. |

### Возвращаемое значение

Масштаб, который был автоматически рассчитан для визуализируемой формы, чтобы соответствовать указанному размеру.

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

* class [NodeRendererBase](../../noderendererbase)
* пространство имен [Aspose.Words.Rendering](../../noderendererbase)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
