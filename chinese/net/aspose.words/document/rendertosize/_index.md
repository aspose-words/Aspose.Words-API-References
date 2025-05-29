---
title: Document.RenderToSize
linktitle: RenderToSize
articleTitle: RenderToSize
second_title: Aspose.Words for .NET
description: 探索 RenderToSize 方法，高效地将文档页面转换为所需尺寸的 Graphics 对象。立即增强您的渲染流程！
type: docs
weight: 740
url: /zh/net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

将文档页面渲染为Graphics对象到指定的大小。

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pageIndex | Int32 | 从 0 开始的页面索引。 |
| graphics | Graphics | 要渲染到的对象。 |
| x | Single | 所呈现页面左上角的 X 坐标（以世界单位为单位）。 |
| y | Single | 所呈现页面左上角的 Y 坐标（以世界单位为单位）。 |
| width | Single | 所呈现的页面可占用的最大宽度（以世界单位为单位）。 |
| height | Single | 所呈现的页面可以占用的最大高度（以世界单位为单位）。 |

### 返回值

自动计算呈现的页面的比例以适合指定的尺寸。

## 例子

展示如何将文档呈现为指定位置和大小的位图（.NetStandard 2.0）。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // 对我们将使用此画布渲染的页面应用 70% 的缩放系数。
        canvas.Scale(70);

        // 将页面从页面的顶部和左侧边缘偏移 0.5 英寸。
        canvas.Translate(0.5f, 0.5f);

        // 将渲染的页面旋转 10 度。
        canvas.RotateDegrees(10);

        // 创建并绘制一个矩形。
        SKRect rect = new SKRect(0f, 0f, 3f, 3f);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 3f / 72f
        });

        // 将文档的第一页渲染为与上述矩形相同的大小。
        // 矩形将构成此页面。
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // 重置矩阵，然后应用一组新的缩放和平移。
        canvas.ResetMatrix();
        canvas.Scale(5);
        canvas.Translate(10, 10);

        // 创建另一个矩形。
        rect = new SKRect(0, 0, 50, 100);
        rect.Offset(90, 10);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 1
        });

        // 再次在新创建的矩形内渲染第一页。
        doc.RenderToSize(0, canvas, 90, 10, 50, 100);

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.RenderToSizeNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

展示如何将文档呈现为指定位置和大小的位图。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // 将“PageUnit”属性设置为“GraphicsUnit.Inch”以使用英寸作为
        // 我们将定义的任何变换和维度的测量单位。
        gr.PageUnit = GraphicsUnit.Inch;

        // 将输出偏移边缘 0.5 英寸。
        gr.TranslateTransform(0.5f, 0.5f);

        // 将输出旋转 10 度。
        gr.RotateTransform(10);

        // 绘制一个 3"x3" 的矩形。
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // 以与矩形相同的尺寸和变换绘制文档的第一页。
        // 矩形将构成第一页的框架。
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // 这是 RenderToSize 方法应用于第一页以适应指定大小的缩放因子。
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // 将“PageUnit”属性设置为“GraphicsUnit.Millimeter”，以毫米为单位
        // 我们将定义的任何变换和维度的测量单位。
        gr.PageUnit = GraphicsUnit.Millimeter;

        // 重置我们在上一次渲染中使用的转换。
        gr.ResetTransform();

         // 应用另一组转换。
        gr.TranslateTransform(10, 10);
        gr.ScaleTransform(0.5f, 0.5f);
        gr.PageScale = 2f;

        // 创建另一个矩形并使用它来构成文档中的另一个页面。
        gr.DrawRectangle(new Pen(Color.Black, 1), 90, 10, 50, 100);
        doc.RenderToSize(1, gr, 90, 10, 50, 100);

        bmp.Save(ArtifactsDir + "Rendering.RenderToSize.png");
    }
}
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
