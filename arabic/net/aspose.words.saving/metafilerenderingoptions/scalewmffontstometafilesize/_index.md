---
title: MetafileRenderingOptions.ScaleWmfFontsToMetafileSize
second_title: Aspose.Words لمراجع .NET API
description: MetafileRenderingOptions ملكية. الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم قياس الخطوط في ملف تعريف WMF وفقًا لحجم ملف التعريف على الصفحة.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/metafilerenderingoptions/scalewmffontstometafilesize/
---
## MetafileRenderingOptions.ScaleWmfFontsToMetafileSize property

الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم قياس الخطوط في ملف تعريف WMF وفقًا لحجم ملف التعريف على الصفحة.

```csharp
public bool ScaleWmfFontsToMetafileSize { get; set; }
```

### ملاحظات

عند عرض ملفات تعريف WMF في MS Word ، قد يتم قياس الخطوط وفقًا لحجم ملف التعريف الفعلي على الصفحة.

عندما يتم تعيين هذه القيمة على`حقيقي`، Aspose.Words تحجيم الخط وفقًا لحجم ملف التعريف على الصفحة.

عندما يتم تعيين هذه القيمة على`خاطئة`يعرض Aspose.Words الخطوط حيث يتم تحويل ملف التعريف إلى حجمه الافتراضي.

يتم استخدام هذا الخيار فقط عندما يتم تقديم ملف التعريف كرسومات متجهة.

النظام الأساسي`حقيقي`.

### أمثلة

يوضح كيفية تغيير حجم خطوط WMF وفقًا لحجم ملف التعريف على الصفحة.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// قم بتعيين خاصية "ScaleWmfFontsToMetafileSize" على "true" لتوسيع نطاق الخطوط
// أن تنسيق النص داخل صور WMF وفقًا لحجم ملف التعريف على الصفحة.
// قم بتعيين الخاصية "ScaleWmfFontsToMetafileSize" على "false" إلى
// احتفظ بالمقياس الافتراضي لهذه الخطوط.
saveOptions.MetafileRenderingOptions.ScaleWmfFontsToMetafileSize = scaleWmfFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.FontsScaledToMetafileSize.pdf", saveOptions);
```

### أنظر أيضا

* class [MetafileRenderingOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../metafilerenderingoptions/)
* المجسم [Aspose.Words](../../../)


