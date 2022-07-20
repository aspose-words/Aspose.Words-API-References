---
title: ShapeRenderer
second_title: Referencia de API de Aspose.Words para .NET
description: Proporciona métodos para representar a un individuoShape../aspose.words.drawing/shape oGroupShape../aspose.words.drawing/groupshape a una imagen rasterizada o vectorial o a un objeto Graphics.
type: docs
weight: 4330
url: /es/net/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class

Proporciona métodos para representar a un individuo[`Shape`](../../aspose.words.drawing/shape) o[`GroupShape`](../../aspose.words.drawing/groupshape) a una imagen rasterizada o vectorial o a un objeto Graphics.

```csharp
public class ShapeRenderer : NodeRendererBase
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [ShapeRenderer](shaperenderer)(ShapeBase) | Inicializa una nueva instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints) { get; } | Obtiene los límites reales de la forma en puntos. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints) { get; } | Obtiene los límites opacos de la forma en puntos. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints) { get; } | Obtiene el tamaño real de la forma en puntos. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels)(float, float) | Calcula los límites de la forma en píxeles para un factor de zoom y una resolución específicos. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels)(float, float, float) | Calcula los límites de la forma en píxeles para un factor de zoom y una resolución específicos. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels)(float, float) | Calcula los límites opacos de la forma en píxeles para un factor de zoom y una resolución específicos. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels)(float, float, float) | Calcula los límites opacos de la forma en píxeles para un factor de zoom y una resolución específicos. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels)(float, float) | Calcula el tamaño de la forma en píxeles para un factor de zoom y resolución especificados. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels)(float, float, float) | Calcula el tamaño de la forma en píxeles para un factor de zoom y resolución especificados. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale)(Graphics, float, float, float) | Convierte la forma en unGraphics objeto a una escala especificada. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize)(Graphics, float, float, float, float) | Convierte la forma en unGraphics objeto a un tamaño especificado. |
| [Save](../../aspose.words.rendering/noderendererbase/save)(Stream, ImageSaveOptions) | Representa la forma en una imagen y la guarda en una secuencia. |
| [Save](../../aspose.words.rendering/noderendererbase/save)(string, ImageSaveOptions) | Representa la forma en una imagen y la guarda en un archivo. |

### Ejemplos

Muestra cómo representar una forma con un objeto Graphics y mostrarla mediante un Windows Form.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    ShapeForm shapeForm = new ShapeForm(new Size(1017, 840));

    // A continuación hay dos formas de usar la clase "ShapeRenderer" para representar una forma en un objeto Graphics.
    // 1 - Crea una forma con un gráfico y renderízala a una escala específica.
    Chart chart = builder.InsertChart(ChartType.Pie, 500, 400).Chart;
    chart.Series.Clear();
    chart.Series.Add("Desktop Browser Market Share (Oct. 2020)",
        new[] { "Google Chrome", "Apple Safari", "Mozilla Firefox", "Microsoft Edge", "Other" },
        new[] { 70.33, 8.87, 7.69, 5.83, 7.28 });

    Shape chartShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    shapeForm.AddShapeToRenderToScale(chartShape, 0, 0, 1.5f);

    // 2 - Crea un grupo de formas y renderízalo a un tamaño específico.
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
/// Renderiza y muestra una lista de formas.
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

### Ver también

* class [NodeRendererBase](../noderendererbase)
* espacio de nombres [Aspose.Words.Rendering](../../aspose.words.rendering)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->