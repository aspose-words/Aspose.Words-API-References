---
title: ShapeRenderer Class
linktitle: ShapeRenderer
articleTitle: ShapeRenderer
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Rendering.ShapeRenderer för att enkelt konvertera former och gruppformer till högkvalitativa raster- eller vektorbilder för dina projekt.
type: docs
weight: 5320
url: /sv/net/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class

Tillhandahåller metoder för att rendera en individ[`Shape`](../../aspose.words.drawing/shape/) eller[`GroupShape`](../../aspose.words.drawing/groupshape/) till en raster- eller vektorbild eller till ett grafikobjekt.

För att lära dig mer, besök[Arbeta med former](https://docs.aspose.com/words/net/working-with-shapes/) dokumentationsartikel.

```csharp
public class ShapeRenderer : NodeRendererBase
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [ShapeRenderer](shaperenderer/)(*[ShapeBase](../../aspose.words.drawing/shapebase/)*) | Initierar en ny instans av den här klassen. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | Hämtar formens faktiska gränser i punkter. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | Hämtar formens ogenomskinliga gränser i punkter. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | Hämtar formens faktiska storlek i punkter. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(*float, float*) | Beräknar formens gränser i pixlar för en angiven zoomfaktor och upplösning. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(*float, float, float*) | Beräknar formens gränser i pixlar för en angiven zoomfaktor och upplösning. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(*float, float*) | Beräknar formens ogenomskinliga gränser i pixlar för en angiven zoomfaktor och upplösning. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(*float, float, float*) | Beräknar formens ogenomskinliga gränser i pixlar för en angiven zoomfaktor och upplösning. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(*float, float*) | Beräknar formens storlek i pixlar för en angiven zoomfaktor och upplösning. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(*float, float, float*) | Beräknar formens storlek i pixlar för en angiven zoomfaktor och upplösning. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(*Graphics, float, float, float*) | Återger formen till enGraphics objekt till en specificerad skala. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(*Graphics, float, float, float, float*) | Återger formen till enGraphics objekt till en angiven storlek. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Renderar formen till en bild och sparar i en ström. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*Stream, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Renderar formen till en SVG-bild och sparar i en dataström. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Renderar formen till en bild och sparar den i en fil. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*string, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Återger formen till en SVG-bild och sparar den i en fil. |

## Exempel

Visar hur man renderar en form med ett grafikobjekt och visar den med hjälp av ett Windows-formulär.

```csharp
public void RenderShapesOnForm()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    ShapeForm shapeForm = new ShapeForm(new Size(1017, 840));

    // Nedan följer två sätt att använda klassen "ShapeRenderer" för att rendera en form till ett Graphics-objekt.
    // 1 - Skapa en form med ett diagram och rendera den till en specifik skala.
    Chart chart = builder.InsertChart(ChartType.Pie, 500, 400).Chart;
    chart.Series.Clear();
    chart.Series.Add("Desktop Browser Market Share (Oct. 2020)",
        new[] { "Google Chrome", "Apple Safari", "Mozilla Firefox", "Microsoft Edge", "Other" },
        new[] { 70.33, 8.87, 7.69, 5.83, 7.28 });

    Shape chartShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    shapeForm.AddShapeToRenderToScale(chartShape, 0, 0, 1.5f);

    // 2 - Skapa en formgrupp och rendera den till en specifik storlek.
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
/// Renderar och visar en lista med former.
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

    private readonly List<KeyValuePair<ShapeBase, float[]>> mShapesToRender;
}
```

### Se även

* class [NodeRendererBase](../noderendererbase/)
* namnutrymme [Aspose.Words.Rendering](../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../)
