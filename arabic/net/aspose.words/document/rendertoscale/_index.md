---
title: Document.RenderToScale
linktitle: RenderToScale
articleTitle: RenderToScale
second_title: Aspose.Words لـ .NET
description: Document RenderToScale طريقة. يعرض صفحة المستند إلى ملفGraphics كائن بمقياس محدد في C#.
type: docs
weight: 680
url: /ar/net/aspose.words/document/rendertoscale/
---
## Document.RenderToScale method

يعرض صفحة المستند إلى ملفGraphics كائن بمقياس محدد.

```csharp
public SizeF RenderToScale(int pageIndex, Graphics graphics, float x, float y, float scale)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pageIndex | Int32 | فهرس الصفحات المستند إلى 0. |
| graphics | Graphics | الكائن الذي سيتم تقديمه إليه. |
| x | Single | الإحداثي X (بالوحدات العالمية) للزاوية العلوية اليسرى من الصفحة المعروضة. |
| y | Single | الإحداثي Y (بالوحدات العالمية) للزاوية العلوية اليسرى من الصفحة المعروضة. |
| scale | Single | مقياس عرض الصفحة (1.0 هو 100%). |

### قيمة الإرجاع

العرض والارتفاع (بالوحدات العالمية) للصفحة المعروضة.

## أمثلة

يوضح كيفية تحويل الصفحات الفردية للمستند إلى رسومات لإنشاء صورة واحدة مع صور مصغرة لجميع الصفحات.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// احسب عدد الصفوف والأعمدة التي سنملأها بالصور المصغرة.
const int thumbColumns = 2;
int thumbRows = Math.DivRem(doc.PageCount, thumbColumns, out int remainder);

if (remainder > 0)
    thumbRows++;

// قم بقياس الصور المصغرة بالنسبة لحجم الصفحة الأولى.
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

        // املأ الخلفية الشفافة باللون الأبيض بشكل افتراضي.
        gr.FillRectangle(new SolidBrush(Color.White), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = Math.DivRem(pageIndex, thumbColumns, out int columnIdx);

            // حدد المكان الذي نريد أن تظهر فيه الصورة المصغرة.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            // اعرض الصفحة كصورة مصغرة، ثم ضعها في إطار مستطيل بنفس الحجم.
            SizeF size = doc.RenderToScale(pageIndex, gr, thumbLeft, thumbTop, scale);
            gr.DrawRectangle(Pens.Black, thumbLeft, thumbTop, size.Width, size.Height);
        }

        img.Save(ArtifactsDir + "Rendering.Thumbnails.png");
    }
}
```

يعرض الصفحات الفردية على شكل رسومات لإنشاء صورة واحدة تحتوي على صور مصغرة لجميع الصفحات (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// احسب عدد الصفوف والأعمدة التي سنملأها بالصور المصغرة.
const int thumbnailColumnsNum = 2;
int thumbRows = Math.DivRem(doc.PageCount, thumbnailColumnsNum, out int remainder);

if (remainder > 0)
    thumbRows++;

 // قم بقياس الصور المصغرة بالنسبة لحجم الصفحة الأولى.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// احسب حجم الصورة التي ستحتوي على جميع الصور المصغرة.
int imgWidth = thumbSize.Width * thumbnailColumnsNum;
int imgHeight = thumbSize.Height * thumbRows;

using (SKBitmap bitmap = new SKBitmap(imgWidth, imgHeight))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // املأ الخلفية الشفافة باللون الأبيض بشكل افتراضي.
        canvas.Clear(SKColors.White);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = Math.DivRem(pageIndex, thumbnailColumnsNum, out int columnIdx);

            // حدد المكان الذي نريد أن تظهر فيه الصورة المصغرة.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            SizeF size = doc.RenderToScale(pageIndex, canvas, thumbLeft, thumbTop, scale);

            // اعرض الصفحة كصورة مصغرة، ثم ضعها في إطار مستطيل بنفس الحجم.
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
