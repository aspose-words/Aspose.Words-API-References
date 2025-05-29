---
title: Document.RenderToScale
linktitle: RenderToScale
articleTitle: RenderToScale
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة RenderToScale لتقديم صفحات المستندات بكفاءة إلى كائنات رسومية بالمقياس المطلوب للحصول على نتائج مرئية مثالية.
type: docs
weight: 730
url: /ar/net/aspose.words/document/rendertoscale/
---
## Document.RenderToScale method

يعرض صفحة مستند فيGraphics الكائن إلى مقياس محدد.

```csharp
public SizeF RenderToScale(int pageIndex, Graphics graphics, float x, float y, float scale)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pageIndex | Int32 | فهرس الصفحة المبني على 0. |
| graphics | Graphics | الكائن الذي سيتم تقديمه إليه. |
| x | Single | إحداثيات X (بالوحدات العالمية) في الزاوية العلوية اليسرى من الصفحة المرسومة. |
| y | Single | إحداثيات Y (بالوحدات العالمية) في الزاوية العلوية اليسرى من الصفحة المرسومة. |
| scale | Single | مقياس عرض الصفحة (1.0 هو 100%). |

### قيمة الإرجاع

العرض والارتفاع (بالوحدات العالمية) للصفحة المقدمة.

## أمثلة

يوضح كيفية تحويل الصفحات الفردية للمستند إلى رسومات لإنشاء صورة واحدة تحتوي على صور مصغرة لجميع الصفحات.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// احسب عدد الصفوف والأعمدة التي سنملأها بالصور المصغرة.
const int thumbColumns = 2;
int thumbRows = doc.PageCount / thumbColumns;
int remainder = doc.PageCount % thumbColumns;

if (remainder > 0)
    thumbRows++;

// قم بتغيير حجم الصور المصغرة بالنسبة لحجم الصفحة الأولى.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// احسب حجم الصورة التي ستحتوي على جميع الصور المصغرة.
int imgWidth = thumbSize.Width * thumbColumns;
int imgHeight = thumbSize.Height * thumbRows;

using (Bitmap img = new Bitmap(imgWidth, imgHeight))
{
    using (Graphics gr = Graphics.FromImage(img))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // املأ الخلفية، والتي تكون شفافة بشكل افتراضي، باللون الأبيض.
        gr.FillRectangle(new SolidBrush(Color.White), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = pageIndex / thumbColumns;
            int columnIdx = pageIndex % thumbColumns;

            // حدد المكان الذي نريد أن تظهر فيه الصورة المصغرة.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            // عرض الصفحة كصورة مصغرة، ثم وضعها في إطار مستطيل بنفس الحجم.
            SizeF size = doc.RenderToScale(pageIndex, gr, thumbLeft, thumbTop, scale);
            gr.DrawRectangle(Pens.Black, thumbLeft, thumbTop, size.Width, size.Height);
        }

        img.Save(ArtifactsDir + "Rendering.Thumbnails.png");
    }
}
```

يقوم بتحويل الصفحات الفردية إلى رسومات لإنشاء صورة واحدة تحتوي على صور مصغرة لجميع الصفحات (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// احسب عدد الصفوف والأعمدة التي سنملأها بالصور المصغرة.
const int thumbnailColumnsNum = 2;
int thumbRows = doc.PageCount / thumbnailColumnsNum;
int remainder = doc.PageCount % thumbnailColumnsNum;

if (remainder > 0)
    thumbRows++;

 // قم بتغيير حجم الصور المصغرة بالنسبة لحجم الصفحة الأولى.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// احسب حجم الصورة التي ستحتوي على جميع الصور المصغرة.
int imgWidth = thumbSize.Width * thumbnailColumnsNum;
int imgHeight = thumbSize.Height * thumbRows;

using (SKBitmap bitmap = new SKBitmap(imgWidth, imgHeight))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // املأ الخلفية، والتي تكون شفافة بشكل افتراضي، باللون الأبيض.
        canvas.Clear(SKColors.White);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = pageIndex / thumbnailColumnsNum;
            int columnIdx = pageIndex % thumbnailColumnsNum;

            // حدد المكان الذي نريد أن تظهر فيه الصورة المصغرة.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            SizeF size = doc.RenderToScale(pageIndex, canvas, thumbLeft, thumbTop, scale);

            // عرض الصفحة كصورة مصغرة، ثم وضعها في إطار مستطيل بنفس الحجم.
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

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
