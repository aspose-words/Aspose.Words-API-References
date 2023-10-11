---
title: Document.RenderToSize
second_title: Aspose.Words for .NET API 参考
description: Document 方法. 将文档页面呈现为Graphics指定大小的对象
type: docs
weight: 710
url: /zh/net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

将文档页面呈现为Graphics指定大小的对象。

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pageIndex | Int32 | 从 0 开始的页面索引。 |
| graphics | Graphics | 渲染到的对象。 |
| x | Single | 渲染页面左上角的 X 坐标（以世界单位表示）。 |
| y | Single | 渲染页面左上角的 Y 坐标（以世界单位表示）。 |
| width | Single | 渲染页面可以占用的最大宽度（以世界单位为单位）。 |
| height | Single | 渲染页面可以占据的最大高度（以世界单位为单位）。 |

### 返回值

自动计算渲染页面以适合指定尺寸的比例。

### 例子

演示如何将文档呈现为指定位置和大小的位图 (.NetStandard 2.0)。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // 将 70% 的缩放系数应用于我们将使用此画布呈现的页面。
        canvas.Scale(70);

        // 将页面从页面的顶部和左侧边缘偏移 0.5"。
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

        // 将文档的第一页渲染为与上面矩形相同的大小。
        // 矩形将构成该页面。
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

        // 再次渲染新创建的矩形内的第一页。
        doc.RenderToSize(0, canvas, 90, 10, 50, 100);

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.RenderToSizeNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

演示如何将文档渲染为指定位置和大小的位图。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // 将“PageUnit”属性设置为“GraphicsUnit.Inch”以使用英寸作为
        // 我们将定义的任何转换和尺寸的测量单位。
        gr.PageUnit = GraphicsUnit.Inch;

        // 将输出从边缘偏移 0.5"。
        gr.TranslateTransform(0.5f, 0.5f);

        // 将输出旋转 10 度。
        gr.RotateTransform(10);

        // 绘制一个 3"x3" 的矩形。
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // 使用与矩形相同的尺寸和变换绘制文档的第一页。
        // 矩形将构成第一页。
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // 这是 RenderToSize 方法应用于第一页以适合指定大小的缩放因子。
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // 将“PageUnit”属性设置为“GraphicsUnit.Millimeter”以使用毫米作为单位
        // 我们将定义的任何转换和尺寸的测量单位。
        gr.PageUnit = GraphicsUnit.Millimeter;

        // 重置我们在之前的渲染中使用的转换。
        gr.ResetTransform();

        // 应用另一组转换。
        gr.TranslateTransform(10, 10);
        gr.ScaleTransform(0.5f, 0.5f);
        gr.PageScale = 2f;

        // 创建另一个矩形并用它来构建文档中的另一个页面。
        gr.DrawRectangle(new Pen(Color.Black, 1), 90, 10, 50, 100);
        doc.RenderToSize(1, gr, 90, 10, 50, 100);

        bmp.Save(ArtifactsDir + "Rendering.RenderToSize.png");
    }
}
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)


