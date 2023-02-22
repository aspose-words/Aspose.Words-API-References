---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
second_title: Aspose.Words لمراجع .NET API
description: MetafileRenderingOptions ملكية. الحصول على أو تعيين قيمة تحدد كيفية عرض EMF  Dual metafiles .
type: docs
weight: 20
url: /ar/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

الحصول على أو تعيين قيمة تحدد كيفية عرض EMF + Dual metafiles .

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

### ملاحظات

تحتوي ملفات التعريف EMF + Dual على أجزاء EMF + و EMF. يعرض MS Word و GDI + دائمًا جزء EMF + . Aspose.word لا تدعم حاليًا جميع سجلات EMF + بشكل كامل وفي بعض الحالات تبدو نتيجة عرض جزء EMF أفضل من نتيجة عرض جزء EMF +.

يتم استخدام هذا الخيار فقط عندما يتم تقديم ملف التعريف كرسومات متجهة. عندما يتم تقديم ملف التعريف إلى صورة نقطية ، يتم دائمًا استخدام جزء EMF +.

النظام الأساسيEmfPlusWithFallback.

### أمثلة

يوضح كيفية تكوين خيارات العرض ذات الصلة بملف تعريف Windows المحسن عند الحفظ في ملف PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// تعيين خاصية "EmfPlusDualRenderingMode" على "EmfPlusDualRenderingMode.Emf"
// لعرض جزء EMF من ملف تعريف EMF + مزدوج فقط.
// قم بتعيين خاصية "EmfPlusDualRenderingMode" على "EmfPlusDualRenderingMode.EmfPlus" إلى
// لتقديم EMF + جزء من ملف تعريف EMF + مزدوج.
// قم بتعيين خاصية "EmfPlusDualRenderingMode" على "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// لتقديم EMF + جزء من ملف تعريف EMF + مزدوج إذا كانت جميع سجلات EMF + مدعومة.
// خلاف ذلك ، ستعرض Aspose.Words جزء EMF.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// اضبط خاصية "UseEmfEmbeddedToWmf" على "true" لعرض بيانات EMF المضمنة
// لملفات التعريف التي يمكننا تقديمها كرسومات متجهة.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### أنظر أيضا

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../metafilerenderingoptions/)
* المجسم [Aspose.Words](../../../)


