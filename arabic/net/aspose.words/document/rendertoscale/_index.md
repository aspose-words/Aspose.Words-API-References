---
title: Document.RenderToScale
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. يعرض صفحة مستند إلى ملفGraphics كائن لمقياس محدد .
type: docs
weight: 660
url: /ar/net/aspose.words/document/rendertoscale/
---
## Document.RenderToScale method

يعرض صفحة مستند إلى ملفGraphics كائن لمقياس محدد .

```csharp
public SizeF RenderToScale(int pageIndex, Graphics graphics, float x, float y, float scale)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pageIndex | Int32 | فهرس الصفحة المستند إلى 0. |
| graphics | Graphics | الكائن الذي يتم تقديمه إليه. |
| x | Single | إحداثي X (بوحدات العالم) أعلى الزاوية اليسرى من الصفحة المعروضة. |
| y | Single | إحداثي Y (بوحدات العالم) أعلى الزاوية اليسرى من الصفحة المقدمة. |
| scale | Single | مقياس عرض الصفحة (1.0 هو 100٪). |

### قيمة الإرجاع

العرض والارتفاع (بوحدات العالم) للصفحة المعروضة.

### أمثلة

يوضح كيفية الصفحات الفردية من المستند إلى الرسومات لإنشاء صورة واحدة باستخدام الصور المصغرة لكل الصفحات.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// احسب عدد الصفوف والأعمدة التي سنملأها بالصور المصغرة.
const int thumbColumns = 2;
int thumbRows = Math.DivRem(doc.PageCount, thumbColumns, out int remainder);

if (remainder > 0)
    thumbRows++;

// مقياس الصور المصغرة بالنسبة إلى حجم الصفحة الأولى.
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

        // املأ الخلفية ، التي تكون شفافة بشكل افتراضي ، باللون الأبيض.
        gr.FillRectangle(new SolidBrush(Color.White), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = Math.DivRem(pageIndex, thumbColumns, out int columnIdx);

            // حدد المكان الذي نريد أن تظهر فيه الصورة المصغرة.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            // اعرض الصفحة كصورة مصغرة ، ثم قم بتأطيرها في مستطيل بالحجم نفسه.
            SizeF size = doc.RenderToScale(pageIndex, gr, thumbLeft, thumbTop, scale);
            gr.DrawRectangle(Pens.Black, thumbLeft, thumbTop, size.Width, size.Height);
        }

        img.Save(ArtifactsDir + "Rendering.Thumbnails.png");
    }
}
```

يجسد الصفحات الفردية للرسومات لإنشاء صورة واحدة مع الصور المصغرة لجميع الصفحات (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// احسب عدد الصفوف والأعمدة التي سنملأها بالصور المصغرة.
const int thumbnailColumnsNum = 2;
int thumbRows = Math.DivRem(doc.PageCount, thumbnailColumnsNum, out int remainder);

if (remainder > 0)
    thumbRows++;

 // مقياس الصور المصغرة بالنسبة إلى حجم الصفحة الأولى.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// احسب حجم الصورة التي ستحتوي على جميع الصور المصغرة.
int imgWidth = thumbSize.Width * thumbnailColumnsNum;
int imgHeight = thumbSize.Height * thumbRows;

using (SKBitmap bitmap = new SKBitmap(imgWidth, imgHeight))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // املأ الخلفية ، التي تكون شفافة بشكل افتراضي ، باللون الأبيض.
        canvas.Clear(SKColors.White);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = Math.DivRem(pageIndex, thumbnailColumnsNum, out int columnIdx);

            // حدد المكان الذي نريد أن تظهر فيه الصورة المصغرة.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            SizeF size = doc.RenderToScale(pageIndex, canvas, thumbLeft, thumbTop, scale);

            // اعرض الصفحة كصورة مصغرة ، ثم قم بتأطيرها في مستطيل بالحجم نفسه.
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
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


