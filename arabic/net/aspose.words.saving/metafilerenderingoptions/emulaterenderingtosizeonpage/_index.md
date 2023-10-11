---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
second_title: Aspose.Words لمراجع .NET API
description: MetafileRenderingOptions ملكية. الحصول على قيمة أو تعيينها لتحديد ما إذا كان عرض ملف التعريف يحاكي عرض ملف التعريف وفقًا للحجم الموجود على page أو عرض ملف التعريف بحجمه الافتراضي.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

الحصول على قيمة أو تعيينها لتحديد ما إذا كان عرض ملف التعريف يحاكي عرض ملف التعريف وفقًا للحجم الموجود على page أو عرض ملف التعريف بحجمه الافتراضي.

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

### ملاحظات

عندما يتم عرض ملفات التعريف في برنامج MS Word، قد يتم تغيير حجم بعض الرسومات وفقًا لحجم ملف التعريف الفعلي بالبكسل. أي أن التكبير/التصغير قد يؤثر على عرض ملف التعريف.

عندما يتم ضبط هذه القيمة على`حقيقي`، يحاكي Aspose.Words العرض وفقًا لحجم ملف التعريف في الصفحة. يتم حساب الحجم بالبكسل من حجم ملف التعريف في الصفحة والمحدد[`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/).

عندما يتم ضبط هذه القيمة على`خطأ شنيع`، Aspose.Words يحاكي عرض ملف التعريف إلى حجمه الافتراضي بالبكسل.

يتم استخدام هذا الخيار فقط عندما يتم عرض ملف التعريف كرسومات متجهة.

القيمة الافتراضية هي`حقيقي`.

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


