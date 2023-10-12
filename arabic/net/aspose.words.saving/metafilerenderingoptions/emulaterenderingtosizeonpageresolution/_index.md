---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
second_title: Aspose.Words لمراجع .NET API
description: MetafileRenderingOptions ملكية. الحصول على الدقة بالبكسل في البوصة أو تعيينها لمحاكاة عرض ملف التعريف حسب الحجم الموجود على الصفحة.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

الحصول على الدقة بالبكسل في البوصة أو تعيينها لمحاكاة عرض ملف التعريف حسب الحجم الموجود على الصفحة.

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

### ملاحظات

يستخدم هذا الخيار فقط عندما[`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/) تم ضبطه على`حقيقي`.

القيمة الافتراضية هي 96. وهذا هو دقة العرض الافتراضية. على سبيل المثال، فإن عرض ملف التعريف سوف يحاكي عرض ملف التعريف في برنامج MS Word مع عامل تكبير بنسبة 100%.

### أمثلة

يوضح كيفية عرض ملف التعريف وفقًا لحجم الصفحة.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// قم بتعيين خاصية "EmulateRenderingToSizeOnPage" على "صحيح"
// لمحاكاة العرض وفقًا لحجم ملف التعريف الموجود على الصفحة.
// قم بتعيين خاصية "EmulateRenderingToSizeOnPage" على "خطأ"
// لمحاكاة عرض ملف التعريف إلى حجمه الافتراضي بالبكسل.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### أنظر أيضا

* class [MetafileRenderingOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../metafilerenderingoptions/)
* المجسم [Aspose.Words](../../../)


