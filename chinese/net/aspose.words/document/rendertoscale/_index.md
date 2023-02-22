---
title: Document.RenderToScale
second_title: Aspose.Words for .NET API 参考
description: Document 方法. 将文档页面呈现为Graphics对象到指定的比例
type: docs
weight: 660
url: /zh/net/aspose.words/document/rendertoscale/
---
## Document.RenderToScale method

将文档页面呈现为Graphics对象到指定的比例。

```csharp
public SizeF RenderToScale(int pageIndex, Graphics graphics, float x, float y, float scale)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pageIndex | Int32 | 基于 0 的页面索引。 |
| graphics | Graphics | 渲染到的对象。 |
| x | Single | 渲染页面左上角的 X 坐标（以世界单位为单位）。 |
| y | Single | 渲染页面左上角的 Y 坐标（以世界单位为单位）。 |
| scale | Single | 渲染页面的比例（1.0 为 100%）。 |

### 返回值

呈现页面的宽度和高度（以世界单位为单位）。

### 例子

演示如何将文档的各个页面转换为图形以创建一个包含所有页面缩略图的图像。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 计算我们将用缩略图填充的行数和列数。
const int thumbColumns = 2;
int thumbRows = Math.DivRem(doc.PageCount, thumbColumns, out int remainder);

if (remainder > 0)
    thumbRows++;

// 相对于第一页的大小缩放缩略图。
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// 计算将包含所有缩略图的图像的大小。
int imgWidth = thumbSize.Width * thumbColumns;
int imgHeight = thumbSize.Height * thumbRows;

using (Bitmap img = new Bitmap(imgWidth, imgHeight))
{
    using (Graphics gr = Graphics.FromImage(img))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // 将默认透明的背景填充为白色。
        gr.FillRectangle(new SolidBrush(Color.White), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = Math.DivRem(pageIndex, thumbColumns, out int columnIdx);

            // 指定我们希望缩略图出现的位置。
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            // 将页面渲染为缩略图，然后将其框在相同大小的矩形中。
            SizeF size = doc.RenderToScale(pageIndex, gr, thumbLeft, thumbTop, scale);
            gr.DrawRectangle(Pens.Black, thumbLeft, thumbTop, size.Width, size.Height);
        }

        img.Save(ArtifactsDir + "Rendering.Thumbnails.png");
    }
}
```

将单个页面渲染为图形以创建一个包含所有页面缩略图的图像 (.NetStandard 2.0)。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 计算我们将用缩略图填充的行数和列数。
const int thumbnailColumnsNum = 2;
int thumbRows = Math.DivRem(doc.PageCount, thumbnailColumnsNum, out int remainder);

if (remainder > 0)
    thumbRows++;

 // 相对于第一页的大小缩放缩略图。
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// 计算将包含所有缩略图的图像的大小。
int imgWidth = thumbSize.Width * thumbnailColumnsNum;
int imgHeight = thumbSize.Height * thumbRows;

using (SKBitmap bitmap = new SKBitmap(imgWidth, imgHeight))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // 将默认透明的背景填充为白色。
        canvas.Clear(SKColors.White);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = Math.DivRem(pageIndex, thumbnailColumnsNum, out int columnIdx);

            // 指定我们希望缩略图出现的位置。
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            SizeF size = doc.RenderToScale(pageIndex, canvas, thumbLeft, thumbTop, scale);

            // 将页面渲染为缩略图，然后将其框在相同大小的矩形中。
            SKRect rect = new SKRect(0, 0, size.Width, size.Height);
            rect.Offset(thumbLeft, thumbTop);
            canvas.DrawRect(rect, new SKPaint
            {
                Color = SKColors.Black,
                Style = SKPaintStyle.Stroke
            });
        }

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.CreateThumbnailsNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)


