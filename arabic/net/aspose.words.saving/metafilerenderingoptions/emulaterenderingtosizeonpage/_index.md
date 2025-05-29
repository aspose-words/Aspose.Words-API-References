---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
linktitle: EmulateRenderingToSizeOnPage
articleTitle: EmulateRenderingToSizeOnPage
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية EmulateRenderingToSizeOnPage على تعزيز عرض الملف التعريفي، مما يضمن أحجام عرض دقيقة للحصول على نتائج مرئية مثالية.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

يحصل على قيمة أو يعينها لتحديد ما إذا كان عرض الملف التعريفي يحاكي عرض الملف التعريفي وفقًا للحجم على page أو عرض الملف التعريفي بحجمه الافتراضي.

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

## ملاحظات

عند عرض ملفات التعريف في MS Word، قد يتم تغيير حجم بعض الرسومات وفقًا لحجم ملف التعريف الفعلي بالبكسل. أي أن التكبير/التصغير قد يؤثر على عرض ملف التعريف.

عندما يتم تعيين هذه القيمة على`حقيقي`يحاكي Aspose.Words عملية العرض وفقًا لحجم الملف التعريفي على الصفحة. يتم حساب الحجم بالبكسل من حجم الملف التعريفي على الصفحة والحجم المحدد[`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/).

عندما يتم تعيين هذه القيمة على`خطأ شنيع`يقوم Aspose.Words بمحاكاة عرض الملف التعريفي إلى حجمه الافتراضي بالبكسل.

يتم استخدام هذا الخيار فقط عندما يتم عرض الملف التعريفي كرسومات متجهة.

القيمة الافتراضية هي`حقيقي`.

## أمثلة

يوضح كيفية عرض الملف التعريفي وفقًا للحجم على الصفحة.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// اضبط خاصية "EmulateRenderingToSizeOnPage" على "true"
// لمحاكاة العرض وفقًا لحجم الملف التعريفي الموجود على الصفحة.
// اضبط خاصية "EmulateRenderingToSizeOnPage" على "false"
// لمحاكاة عرض الملف التعريفي إلى حجمه الافتراضي بالبكسل.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### أنظر أيضا

* class [MetafileRenderingOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
