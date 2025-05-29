---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
linktitle: EmulateRenderingToSizeOnPageResolution
articleTitle: EmulateRenderingToSizeOnPageResolution
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MetafileRenderingOptions EmulateRenderingToSizeOnPageResolution. تحكم في دقة عرض ملف التعريف لعرض الصفحة بشكل مثالي.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

يحصل على الدقة بالبكسل لكل بوصة أو يضبطها لمحاكاة عرض الملف التعريفي إلى الحجم الموجود في الصفحة.

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

## ملاحظات

يتم استخدام هذا الخيار فقط عندما[`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/) تم ضبطه على`حقيقي`.

القيمة الافتراضية هي 96. هذه دقة عرض افتراضية. أي أن عرض ملف التعريف سيُحاكي عرض ملف التعريف في مايكروسوفت وورد بنسبة تكبير 100%.

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
