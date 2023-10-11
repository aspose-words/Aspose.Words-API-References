---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
second_title: Aspose.Words لمراجع .NET API
description: MetafileRenderingOptions ملكية. الحصول على قيمة أو تعيينها لتحديد كيفية عرض ملفات تعريف EMF Dual.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

الحصول على قيمة أو تعيينها لتحديد كيفية عرض ملفات تعريف EMF+ Dual.

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

### ملاحظات

تحتوي ملفات التعريف EMF+ Dual على أجزاء EMF+ وEMF. يقوم MS Word وGDI+ دائمًا بعرض جزء EMF+. Aspose. لا يدعم Words حاليًا جميع سجلات EMF+ بشكل كامل وفي بعض الحالات، يبدو عرض نتيجة جزء EMF أفضل من عرض نتيجة جزء EMF+.

يتم استخدام هذا الخيار فقط عندما يتم عرض ملف التعريف كرسومات متجهة. عندما يتم تقديم ملف التعريف إلى صورة نقطية، يتم دائمًا استخدام جزء EMF+.

القيمة الافتراضية هيEmfPlusWithFallback.

### أمثلة

يوضح كيفية تكوين خيارات العرض ذات الصلة بملف Windows Metafile المحسن عند الحفظ في ملف PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// قم بتعيين خاصية "EmfPlusDualRenderingMode" على "EmfPlusDualRenderingMode.Emf"
// لعرض جزء EMF فقط من ملف التعريف المزدوج EMF+.
// قم بتعيين خاصية "EmfPlusDualRenderingMode" على "EmfPlusDualRenderingMode.EmfPlus" إلى
// لعرض جزء EMF+ من ملف التعريف المزدوج EMF+.
// قم بتعيين خاصية "EmfPlusDualRenderingMode" على "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// لعرض جزء EMF+ من ملف التعريف المزدوج EMF+ إذا كانت جميع سجلات EMF+ مدعومة.
// بخلاف ذلك، سيقوم Aspose.Words بعرض جزء EMF.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// قم بتعيين خاصية "UseEmfEmbeddedToWmf" على "صحيح" لعرض بيانات EMF المضمنة
// لملفات التعريف التي يمكننا تقديمها كرسومات متجهة.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### أنظر أيضا

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../metafilerenderingoptions/)
* المجسم [Aspose.Words](../../../)


