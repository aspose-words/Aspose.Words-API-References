---
title: ShapeRenderer Class
linktitle: ShapeRenderer
articleTitle: ShapeRenderer
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Rendering.ShapeRenderer，轻松将 Shapes 和 GroupShapes 转换为项目的高质量光栅或矢量图像。
type: docs
weight: 5320
url: /zh/net/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class

提供方法来呈现个体[`Shape`](../../aspose.words.drawing/shape/)或者[`GroupShape`](../../aspose.words.drawing/groupshape/) 转换为光栅图像、矢量图像或图形对象。

要了解更多信息，请访问[使用形状的 Working ](https://docs.aspose.com/words/net/working-with-shapes/)文档文章。

```csharp
public class ShapeRenderer : NodeRendererBase
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [ShapeRenderer](shaperenderer/)(*[ShapeBase](../../aspose.words.drawing/shapebase/)*) | 初始化此类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | 获取形状的实际边界（以点为单位）。 |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | 获取形状的不透明边界（以点为单位）。 |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | 获取形状的实际大小（以点为单位）。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(*float, float*) | 计算指定缩放系数和分辨率的形状边界（以像素为单位）。 |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(*float, float, float*) | 计算指定缩放系数和分辨率的形状边界（以像素为单位）。 |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(*float, float*) | 计算指定缩放系数和分辨率的形状的不透明边界（以像素为单位）。 |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(*float, float, float*) | 计算指定缩放系数和分辨率的形状的不透明边界（以像素为单位）。 |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(*float, float*) | 计算指定缩放系数和分辨率的形状大小（以像素为单位）。 |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(*float, float, float*) | 计算指定缩放系数和分辨率的形状大小（以像素为单位）。 |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(*Graphics, float, float, float*) | 将形状渲染为Graphics 对象到指定的比例。 |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(*Graphics, float, float, float, float*) | 将形状渲染为Graphics 对象为指定大小。 |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | 将形状渲染为图像并保存到流中。 |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*Stream, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | 将形状渲染为 SVG 图像并保存到流中。 |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | 将形状渲染为图像并保存到文件中。 |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*string, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | 将形状渲染为 SVG 图像并保存到文件中。 |

## 例子

展示如何使用 Graphics 对象呈现形状并使用 Windows 窗体显示它。

```csharp
public void RenderShapesOnForm()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    ShapeForm shapeForm = new ShapeForm(new Size(1017, 840));

    // 下面是两种使用“ShapeRenderer”类将形状渲染为 Graphics 对象的方法。
    // 1 - 使用图表创建形状，并将其渲染到特定比例。
    Chart chart = builder.InsertChart(ChartType.Pie, 500, 400).Chart;
    chart.Series.Clear();
    chart.Series.Add("Desktop Browser Market Share (Oct. 2020)",
        new[] { "Google Chrome", "Apple Safari", "Mozilla Firefox", "Microsoft Edge", "Other" },
        new[] { 70.33, 8.87, 7.69, 5.83, 7.28 });

    Shape chartShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    shapeForm.AddShapeToRenderToScale(chartShape, 0, 0, 1.5f);

    // 2 - 创建一个形状组，并将其渲染为特定大小。
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
/// 渲染并显示形状列表。
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

### 也可以看看

* class [NodeRendererBase](../noderendererbase/)
* 命名空间 [Aspose.Words.Rendering](../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../)
