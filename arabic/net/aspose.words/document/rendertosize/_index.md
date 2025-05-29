---
title: Document.RenderToSize
linktitle: RenderToSize
articleTitle: RenderToSize
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة RenderToSize لتحويل صفحات المستندات بكفاءة إلى كائنات رسومية بالأبعاد التي تريدها. حسّن عملية العرض لديك اليوم!
type: docs
weight: 740
url: /ar/net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

يعرض صفحة مستند فيGraphics الكائن إلى حجم محدد.

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pageIndex | Int32 | فهرس الصفحة المبني على 0. |
| graphics | Graphics | الكائن الذي سيتم تقديمه إليه. |
| x | Single | إحداثيات X (بالوحدات العالمية) في الزاوية العلوية اليسرى من الصفحة المرسومة. |
| y | Single | إحداثيات Y (بالوحدات العالمية) في الزاوية العلوية اليسرى من الصفحة المرسومة. |
| width | Single | الحد الأقصى للعرض (بالوحدات العالمية) الذي يمكن أن تشغله الصفحة المقدمة. |
| height | Single | الارتفاع الأقصى (بالوحدات العالمية) الذي يمكن أن تشغله الصفحة المقدمة. |

### قيمة الإرجاع

المقياس الذي تم حسابه تلقائيًا للصفحة المقدمة لتناسب الحجم المحدد.

## أمثلة

يوضح كيفية عرض المستند كخريطة نقطية في موقع وحجم محددين (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // قم بتطبيق عامل مقياس بنسبة 70% على الصفحة التي سنقوم بعرضها باستخدام هذه اللوحة القماشية.
        canvas.Scale(70);

        //إزاحة الصفحة بمقدار 0.5 بوصة من الحواف العلوية واليسرى للصفحة.
        canvas.Translate(0.5f, 0.5f);

        // تدوير الصفحة المقدمة بمقدار 10 درجات.
        canvas.RotateDegrees(10);

        // إنشاء مستطيل ورسمه.
        SKRect rect = new SKRect(0f, 0f, 3f, 3f);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 3f / 72f
        });

        // قم بعرض الصفحة الأولى من المستند بنفس حجم المستطيل أعلاه.
        // سوف يقوم المستطيل بتأطير هذه الصفحة.
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // إعادة تعيين المصفوفة، ثم تطبيق مجموعة جديدة من القياسات والترجمات.
        canvas.ResetMatrix();
        canvas.Scale(5);
        canvas.Translate(10, 10);

        // إنشاء مستطيل آخر.
        rect = new SKRect(0, 0, 50, 100);
        rect.Offset(90, 10);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 1
        });

        // قم بعرض الصفحة الأولى داخل المستطيل الذي تم إنشاؤه حديثًا مرة أخرى.
        doc.RenderToSize(0, canvas, 90, 10, 50, 100);

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.RenderToSizeNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

يوضح كيفية عرض مستند إلى خريطة نقطية في موقع وحجم محددين.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // اضبط خاصية "PageUnit" على "GraphicsUnit.Inch" لاستخدام البوصات كوحدة
        // وحدة القياس لأي تحويلات وأبعاد سنقوم بتعريفها.
        gr.PageUnit = GraphicsUnit.Inch;

        //إزاحة الإخراج بمقدار 0.5 بوصة من الحافة.
        gr.TranslateTransform(0.5f, 0.5f);

        // قم بتدوير الإخراج بمقدار 10 درجات.
        gr.RotateTransform(10);

        // ارسم مستطيلًا بمقاس 3 × 3 بوصة.
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // ارسم الصفحة الأولى من مستندنا بنفس الأبعاد والتحويل مثل المستطيل.
        // المستطيل سوف يحيط بالصفحة الأولى.
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // هذا هو عامل القياس الذي طبقته طريقة RenderToSize على الصفحة الأولى لتناسب الحجم المحدد.
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // اضبط خاصية "PageUnit" على "GraphicsUnit.Millimeter" لاستخدام المليمترات كوحدة
        // وحدة القياس لأي تحويلات وأبعاد سنقوم بتعريفها.
        gr.PageUnit = GraphicsUnit.Millimeter;

        // إعادة تعيين التحويلات التي استخدمناها من العرض السابق.
        gr.ResetTransform();

         // تطبيق مجموعة أخرى من التحويلات.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
