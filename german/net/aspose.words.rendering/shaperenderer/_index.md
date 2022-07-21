---
title: ShapeRenderer
second_title: Aspose.Words für .NET-API-Referenz
description: Stellt Methoden bereit um eine Person zu rendernShape../aspose.words.drawing/shape oderGroupShape../aspose.words.drawing/groupshape in ein Raster- oder Vektorbild oder in ein Grafikobjekt.
type: docs
weight: 4330
url: /de/net/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class

Stellt Methoden bereit, um eine Person zu rendern[`Shape`](../../aspose.words.drawing/shape) oder[`GroupShape`](../../aspose.words.drawing/groupshape) in ein Raster- oder Vektorbild oder in ein Grafikobjekt.

```csharp
public class ShapeRenderer : NodeRendererBase
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [ShapeRenderer](shaperenderer)(ShapeBase) | Initialisiert eine neue Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints) { get; } | Ruft die tatsächlichen Grenzen der Form in Punkten ab. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints) { get; } | Ruft die undurchsichtigen Grenzen der Form in Punkten ab. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints) { get; } | Ruft die tatsächliche Größe der Form in Punkten ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels)(float, float) | Berechnet die Grenzen der Form in Pixeln für einen angegebenen Zoomfaktor und eine angegebene Auflösung. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels)(float, float, float) | Berechnet die Grenzen der Form in Pixeln für einen angegebenen Zoomfaktor und eine angegebene Auflösung. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels)(float, float) | Berechnet die undurchsichtigen Grenzen der Form in Pixeln für einen angegebenen Zoomfaktor und eine angegebene Auflösung. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels)(float, float, float) | Berechnet die undurchsichtigen Grenzen der Form in Pixeln für einen angegebenen Zoomfaktor und eine angegebene Auflösung. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels)(float, float) | Berechnet die Größe der Form in Pixeln für einen angegebenen Zoomfaktor und eine angegebene Auflösung. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels)(float, float, float) | Berechnet die Größe der Form in Pixeln für einen angegebenen Zoomfaktor und eine angegebene Auflösung. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale)(Graphics, float, float, float) | Rendert die Form in aGraphics Objekt in einem bestimmten Maßstab. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize)(Graphics, float, float, float, float) | Rendert die Form in aGraphics Objekt auf eine bestimmte Größe. |
| [Save](../../aspose.words.rendering/noderendererbase/save)(Stream, ImageSaveOptions) | Rendert die Form in ein Bild und speichert sie in einem Stream. |
| [Save](../../aspose.words.rendering/noderendererbase/save)(string, ImageSaveOptions) | Rendert die Form in ein Bild und speichert sie in einer Datei. |

### Beispiele

Zeigt, wie eine Form mit einem Graphics-Objekt gerendert und mit einem Windows Form angezeigt wird.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    ShapeForm shapeForm = new ShapeForm(new Size(1017, 840));

    // Im Folgenden finden Sie zwei Möglichkeiten, die "ShapeRenderer"-Klasse zu verwenden, um eine Form in ein Graphics-Objekt zu rendern.
    // 1 - Erstellen Sie eine Form mit einem Diagramm und rendern Sie es in einem bestimmten Maßstab.
    Chart chart = builder.InsertChart(ChartType.Pie, 500, 400).Chart;
    chart.Series.Clear();
    chart.Series.Add("Desktop Browser Market Share (Oct. 2020)",
        new[] { "Google Chrome", "Apple Safari", "Mozilla Firefox", "Microsoft Edge", "Other" },
        new[] { 70.33, 8.87, 7.69, 5.83, 7.28 });

    Shape chartShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    shapeForm.AddShapeToRenderToScale(chartShape, 0, 0, 1.5f);

    // 2 - Erstellen Sie eine Formgruppe und rendern Sie sie auf eine bestimmte Größe.
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
/// Rendert und zeigt eine Liste von Formen an.
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

### Siehe auch

* class [NodeRendererBase](../noderendererbase)
* namensraum [Aspose.Words.Rendering](../../aspose.words.rendering)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
