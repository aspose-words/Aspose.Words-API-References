---
title: ShapeRenderer class
linktitle: ShapeRenderer class
articleTitle: ShapeRenderer class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Rendering.ShapeRenderer class. Provides methods to render an individual [Shape](../../aspose.words.drawing/shape/) or [GroupShape](../../aspose.words.drawing/groupshape/)  to a raster or vector image or to a Graphics object"
type: docs
weight: 40
url: /nodejs-net/aspose.words.rendering/shaperenderer/
---

## ShapeRenderer class

Provides methods to render an individual [Shape](../../aspose.words.drawing/shape/) or [GroupShape](../../aspose.words.drawing/groupshape/) 
to a raster or vector image or to a Graphics object.
To learn more, visit the [Working
            with Shapes](https://docs.aspose.com/words/nodejs-net/working-with-shapes/) documentation article.




**Inheritance:** [ShapeRenderer](./) → [NodeRendererBase](../noderendererbase/)

### Constructors
| Name | Description |
| --- | --- |
| [ShapeRenderer(shape)](./constructor/#shapebase) | Initializes a new instance of this class. |

### Methods

| Name | Description |
| --- | --- |
|[ getBoundsInPixels2(scale, dpi)](../noderendererbase/getBoundsInPixels2/#number_number) | <br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
|[ getBoundsInPixels2(scale, horizontalDpi, verticalDpi)](../noderendererbase/getBoundsInPixels2/#number_number_number) | <br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
|[ getOpaqueBoundsInPixels2(scale, dpi)](../noderendererbase/getOpaqueBoundsInPixels2/#number_number) | <br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
|[ getOpaqueBoundsInPixels2(scale, horizontalDpi, verticalDpi)](../noderendererbase/getOpaqueBoundsInPixels2/#number_number_number) | <br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
|[ save(fileName, saveOptions)](../noderendererbase/save/#string_imagesaveoptions) | Renders the shape into an image and saves into a file.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
|[ save(fileName, saveOptions)](../noderendererbase/save/#string_svgsaveoptions) | Renders the shape into an SVG image and saves into a file.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
|[ save(stream, saveOptions)](../noderendererbase/save/#buffer_imagesaveoptions) | Renders the shape into an image and saves into a stream.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |
|[ save(stream, saveOptions)](../noderendererbase/save/#buffer_svgsaveoptions) | Renders the shape into an SVG image and saves into a stream.<br>(Inherited from [NodeRendererBase](../noderendererbase/)) |

### Examples

Shows how to render a shape with a Graphics object and display it using a Windows Form.

```js
test('RenderShapesOnForm', () => {
  let doc = new aw.Document();
  let builder = new aw.DocumentBuilder(doc);

  let shapeForm = new ShapeForm(new Size(1017, 840));

  // Below are two ways to use the "ShapeRenderer" class to render a shape to a Graphics object.
  // 1 -  Create a shape with a chart, and render it to a specific scale.
  let chart = builder.insertChart(aw.Drawing.Charts.ChartType.Pie, 500, 400).Chart;
  chart.series.clear();
  chart.series.add("Desktop Browser Market Share (Oct. 2020)",
    new[] { "Google Chrome", "Apple Safari", "Mozilla Firefox", "Microsoft Edge", "Other" },
    new[] { 70.33, 8.87, 7.69, 5.83, 7.28 });

  let chartShape = (Shape)doc.getShape(0, true);

  shapeForm.AddShapeToRenderToScale(chartShape, 0, 0, 1.5f);

  // 2 -  Create a shape group, and render it to a specific size.
  let group = new aw.Drawing.GroupShape(doc);
  group.bounds = new RectangleF(0, 0, 100, 100);
  group.coordSize = new aw.Fields.Size(500, 500);

  let subShape = new aw.Drawing.Shape(doc, aw.Drawing.ShapeType.Rectangle);
  subShape.width = 500;
  subShape.height = 500;
  subShape.left = 0;
  subShape.top = 0;
  subShape.fillColor = "#4169E1";
  group.appendChild(subShape);

  subShape = new aw.Drawing.Shape(doc, aw.Drawing.ShapeType.Image);
  subShape.width = 450;
  subShape.height = 450;
  subShape.left = 25;
  subShape.top = 25;
  subShape.imageData.setImage(base.imageDir + "Logo.jpg");
  group.appendChild(subShape);

  builder.insertNode(group);

  let groupShape = (GroupShape)doc.getChild(aw.NodeType.GroupShape, 0, true);
  shapeForm.AddShapeToRenderToSize(groupShape, 880, 680, 100, 100);

  shapeForm.ShowDialog();
});


  /// <summary>
  /// Renders and displays a list of shapes.
  /// </summary>
private class ShapeForm : Form
{
  public ShapeForm(Size size)
  {
    Size = size;
    mShapesToRender = new aw.Lists.List<KeyValuePair<ShapeBase, float[]>>();
  }

  public void AddShapeToRenderToScale(ShapeBase shape, float x, float y, float scale)
  {
    mShapesToRender.add(new KeyValuePair<ShapeBase, float.at(]>(shape, new[) {x, y, scale}));
  }

  public void AddShapeToRenderToSize(ShapeBase shape, float x, float y, float width, float height)
  {
    mShapesToRender.add(new KeyValuePair<ShapeBase, float.at(]>(shape, new[) {x, y, width, height}));
  }

  protected override void OnPaint(PaintEventArgs e)
  {
    foreach (KeyValuePair<ShapeBase, float[]> renderingArgs in mShapesToRender)
      if (renderingArgs.value.length == 3)
        RenderShapeToScale(renderingArgs.Key, renderingArgs.value.at(0), renderingArgs.value.at(1),
          renderingArgs.value.at(2));
      else if (renderingArgs.value.length == 4)
        RenderShapeToSize(renderingArgs.Key, renderingArgs.value.at(0), renderingArgs.value.at(1),
          renderingArgs.value.at(2), renderingArgs.value.at(3));
  }

  private void RenderShapeToScale(ShapeBase shape, float x, float y, float scale)
  {
    let renderer = new aw.Rendering.ShapeRenderer(shape);
    {
      renderer.renderToScale(formGraphics, x, y, scale);
    }
  }

  private void RenderShapeToSize(ShapeBase shape, float x, float y, float width, float height)
  {
    let renderer = new aw.Rendering.ShapeRenderer(shape);
    {
      renderer.renderToSize(formGraphics, x, y, width, height);
    }
  }

  private readonly List<KeyValuePair<ShapeBase, float[]>> mShapesToRender;
}
```

### See Also

* module [Aspose.Words.Rendering](../)
* class [NodeRendererBase](../noderendererbase/)

