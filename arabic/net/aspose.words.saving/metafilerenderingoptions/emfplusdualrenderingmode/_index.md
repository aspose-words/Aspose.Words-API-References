---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية EmfPlusDualRenderingMode عرض ملفات التعريف EMF Dual. حسّن رسوماتك مع خيارات عرض مرنة اليوم!
type: docs
weight: 20
url: /ar/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

يحصل على قيمة تحدد كيفية عرض ملفات التعريف EMF+ Dual أو يعينها.

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

## ملاحظات

تحتوي ملفات التعريف المزدوجة EMF+ على كلٍّ من جزأَي EMF+ وEMF. يقوم MS Word وGDI+ دائمًا بعرض جزء EMF+. لا يدعم Aspose.Words حاليًا جميع سجلات EMF+ بشكل كامل، وفي بعض الحالات، تبدو نتيجة عرض جزء EMF أفضل من نتيجة عرض جزء EMF+.

يُستخدم هذا الخيار فقط عند عرض ملف التعريف كرسومات متجهة. عند عرض ملف التعريف كصورة نقطية، يُستخدم دائمًا الجزء EMF+.

القيمة الافتراضية هيEmfPlusWithFallback.

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

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
