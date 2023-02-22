---
title: Document.RenderToSize
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. يعرض صفحة مستند إلى ملفGraphics كائن لحجم محدد .
type: docs
weight: 670
url: /ar/net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

يعرض صفحة مستند إلى ملفGraphics كائن لحجم محدد .

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pageIndex | Int32 | فهرس الصفحة المستند إلى 0. |
| graphics | Graphics | الكائن الذي يتم تقديمه إليه. |
| x | Single | إحداثي X (بوحدات العالم) أعلى الزاوية اليسرى من الصفحة المعروضة. |
| y | Single | إحداثي Y (بوحدات العالم) أعلى الزاوية اليسرى من الصفحة المقدمة. |
| width | Single | أقصى عرض (بوحدات العالم) يمكن أن تشغله الصفحة المقدمة. |
| height | Single | أقصى ارتفاع (بوحدات العالم) يمكن أن تشغله الصفحة المعروضة. |

### قيمة الإرجاع

المقياس الذي تم حسابه تلقائيًا للصفحة المعروضة لتلائم الحجم المحدد.

### أمثلة

يوضح كيفية عرض المستند كصورة نقطية في موقع وحجم محددين (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // قم بتطبيق عامل تحجيم بنسبة 70٪ على الصفحة التي سنعرضها باستخدام لوحة الرسم هذه.
        canvas.Scale(70);

        // إزاحة الصفحة 0.5 "من الحواف العلوية واليسرى للصفحة.
        canvas.Translate(0.5f, 0.5f);

        // قم بتدوير الصفحة المقدمة بمقدار 10 درجات.
        canvas.RotateDegrees(10);

        // إنشاء ورسم مستطيل.
        SKRect rect = new SKRect(0f, 0f, 3f, 3f);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 3f / 72f
        });

        // تقديم الصفحة الأولى من المستند إلى نفس حجم المستطيل أعلاه.
        // سيؤطر المستطيل هذه الصفحة.
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // أعد تعيين المصفوفة ، ثم طبق مجموعة جديدة من التحجيم والترجمات.
        canvas.ResetMatrix();
        canvas.Scale(5);
        canvas.Translate(10, 10);

        // قم بإنشاء مستطيل آخر.
        rect = new SKRect(0, 0, 50, 100);
        rect.Offset(90, 10);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 1
        });

        // اعرض الصفحة الأولى داخل المستطيل الذي تم إنشاؤه حديثًا مرة أخرى.
        doc.RenderToSize(0, canvas, 90, 10, 50, 100);

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.RenderToSizeNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

يوضح كيفية تقديم مستند إلى صورة نقطية في موقع وحجم محددين.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // اضبط خاصية "PageUnit" على "GraphicsUnit.Inch" لاستخدام البوصة كملف
        // وحدة قياس لأية تحولات وأبعاد سنحددها.
        gr.PageUnit = GraphicsUnit.Inch;

        // إزاحة الناتج 0.5 "من الحافة.
        gr.TranslateTransform(0.5f, 0.5f);

        // قم بتدوير الإخراج بمقدار 10 درجات.
        gr.RotateTransform(10);

        // ارسم مستطيلاً 3 × 3.
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // ارسم الصفحة الأولى من وثيقتنا بنفس الأبعاد والتحول مثل المستطيل.
        // سيؤطر المستطيل الصفحة الأولى.
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // هذا هو عامل القياس الذي طبقته طريقة RenderToSize على الصفحة الأولى لتلائم الحجم المحدد.
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // اضبط خاصية "PageUnit" على "GraphicsUnit.Millimeter" لاستخدام المليمترات على أنها
        // وحدة قياس لأية تحولات وأبعاد سنحددها.
        gr.PageUnit = GraphicsUnit.Millimeter;

        // إعادة تعيين التحويلات التي استخدمناها من العرض السابق.
        gr.ResetTransform();

         // تطبيق مجموعة أخرى من التحولات.
        gr.TranslateTransform(10, 10);
        gr.ScaleTransform(0.5f, 0.5f);
        gr.PageScale = 2f;

        // قم بإنشاء مستطيل آخر واستخدمه لتأطير صفحة أخرى من المستند.
        gr.DrawRectangle(new Pen(Color.Black, 1), 90, 10, 50, 100);
        doc.RenderToSize(1, gr, 90, 10, 50, 100);

        bmp.Save(ArtifactsDir + "Rendering.RenderToSize.png");
    }
}
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


