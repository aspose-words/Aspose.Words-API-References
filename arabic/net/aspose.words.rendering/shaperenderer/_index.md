---
title: ShapeRenderer
second_title: Aspose.Words لمراجع .NET API
description: توفير طرق لتصيير فردShape../aspose.words.drawing/shape أوGroupShape../aspose.words.drawing/groupshape إلى صورة نقطية أو متجهة أو إلى كائن رسومي.
type: docs
weight: 4330
url: /ar/net/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class

توفير طرق لتصيير فرد[`Shape`](../../aspose.words.drawing/shape) أو[`GroupShape`](../../aspose.words.drawing/groupshape) إلى صورة نقطية أو متجهة أو إلى كائن رسومي.

```csharp
public class ShapeRenderer : NodeRendererBase
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [ShapeRenderer](shaperenderer)(ShapeBase) | تهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints) { get; } | يحصل على الحدود الفعلية للشكل بالنقاط . |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints) { get; } | يحصل على الحدود المعتمة للشكل بالنقاط . |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints) { get; } | الحصول على الحجم الفعلي للشكل بالنقاط . |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels)(float, float) | حساب حدود الشكل بالبكسل لعامل تكبير ودقة محددين . |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels)(float, float, float) | حساب حدود الشكل بالبكسل لعامل تكبير ودقة محددين . |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels)(float, float) | لحساب الحدود المعتمة للشكل بالبكسل لعامل تكبير ودقة محددين . |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels)(float, float, float) | لحساب الحدود المعتمة للشكل بالبكسل لعامل تكبير ودقة محددين . |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels)(float, float) | حساب حجم الشكل بالبكسل لعامل تكبير ودقة محددين . |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels)(float, float, float) | حساب حجم الشكل بالبكسل لعامل تكبير ودقة محددين . |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale)(Graphics, float, float, float) | يجعل الشكل في ملفGraphics كائن إلى مقياس محدد . |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize)(Graphics, float, float, float, float) | يجعل الشكل في ملفGraphics كائن لحجم محدد . |
| [Save](../../aspose.words.rendering/noderendererbase/save)(Stream, ImageSaveOptions) | يجسد الشكل في صورة ويحفظ في تدفق . |
| [Save](../../aspose.words.rendering/noderendererbase/save)(string, ImageSaveOptions) | يعرض الشكل في صورة وحفظه في ملف. |

### أمثلة

يوضح كيفية تجسيد شكل باستخدام كائن رسومي وعرضه باستخدام نموذج Windows.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    ShapeForm shapeForm = new ShapeForm(new Size(1017, 840));

    // فيما يلي طريقتان لاستخدام فئة "ShapeRenderer" لتقديم شكل إلى كائن رسومات.
    // 1 - أنشئ شكلًا باستخدام مخطط ، واجعله بمقياس معين.
    Chart chart = builder.InsertChart(ChartType.Pie, 500, 400).Chart;
    chart.Series.Clear();
    chart.Series.Add("Desktop Browser Market Share (Oct. 2020)",
        new[] { "Google Chrome", "Apple Safari", "Mozilla Firefox", "Microsoft Edge", "Other" },
        new[] { 70.33, 8.87, 7.69, 5.83, 7.28 });

    Shape chartShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    shapeForm.AddShapeToRenderToScale(chartShape, 0, 0, 1.5f);

    // 2 - أنشئ مجموعة شكل ، واجعلها بحجم معين.
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
/// يعرض قائمة من الأشكال ويعرضها.
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

### أنظر أيضا

* class [NodeRendererBase](../noderendererbase)
* مساحة الاسم [Aspose.Words.Rendering](../../aspose.words.rendering)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
