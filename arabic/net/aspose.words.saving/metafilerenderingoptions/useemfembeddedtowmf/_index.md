---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
linktitle: UseEmfEmbeddedToWmf
articleTitle: UseEmfEmbeddedToWmf
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية UseEmfEmbeddedToWmf على تحسين عرض ملف WMF، مما يعزز الأداء والجودة لتطبيقات الرسومات الخاصة بك.
type: docs
weight: 70
url: /ar/net/aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/
---
## MetafileRenderingOptions.UseEmfEmbeddedToWmf property

يحصل على قيمة أو يعينها لتحديد كيفية عرض ملفات تعريف WMF التي تحتوي على ملفات تعريف EMF مضمنة.

```csharp
public bool UseEmfEmbeddedToWmf { get; set; }
```

## ملاحظات

قد تحتوي ملفات تعريف WMF على بيانات EMF مُضمَّنة. يستخدم MS Word في أغلب الأحيان بيانات EMF مُضمَّنة. يستخدم GDI+ دائمًا بيانات WMF.

عندما يتم تعيين هذه القيمة على`حقيقي`يستخدم Aspose.Words بيانات EMF المضمنة عند العرض.

عندما يتم تعيين هذه القيمة على`خطأ شنيع`يستخدم Aspose.Words بيانات WMF عند العرض.

يُستخدم هذا الخيار فقط عند عرض ملف التعريف كرسومات متجهة. عند عرض ملف التعريف كصورة نقطية، تُستخدم بيانات WMF دائمًا.

القيمة الافتراضية هي`حقيقي`.

## أمثلة

يوضح كيفية تكوين خيارات العرض المحسنة المرتبطة بملفات Windows Metafile عند الحفظ في PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// اضبط خاصية "EmfPlusDualRenderingMode" إلى "EmfPlusDualRenderingMode.Emf"
// لعرض جزء EMF فقط من ملف التعريف المزدوج EMF+.
// اضبط خاصية "EmfPlusDualRenderingMode" على "EmfPlusDualRenderingMode.EmfPlus" إلى
// لعرض جزء EMF+ من ملف تعريفي مزدوج EMF+.
// اضبط خاصية "EmfPlusDualRenderingMode" إلى "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// لعرض جزء EMF+ من ملف تعريفي مزدوج EMF+ إذا كانت جميع سجلات EMF+ مدعومة.
// خلاف ذلك، سوف يقوم Aspose.Words بعرض جزء EMF.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// اضبط خاصية "UseEmfEmbeddedToWmf" على "true" لعرض بيانات EMF المضمنة
// للملفات التعريفية التي يمكننا تقديمها كرسومات متجهة.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### أنظر أيضا

* class [MetafileRenderingOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
