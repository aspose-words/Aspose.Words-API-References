---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
second_title: Aspose.Words لمراجع .NET API
description: MetafileRenderingOptions ملكية. الحصول على قيمة أو تعيينها لتحديد كيفية عرض ملفات تعريف WMF مع ملفات تعريف EMF المضمنة.
type: docs
weight: 70
url: /ar/net/aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/
---
## MetafileRenderingOptions.UseEmfEmbeddedToWmf property

الحصول على قيمة أو تعيينها لتحديد كيفية عرض ملفات تعريف WMF مع ملفات تعريف EMF المضمنة.

```csharp
public bool UseEmfEmbeddedToWmf { get; set; }
```

### ملاحظات

يمكن أن تحتوي ملفات تعريف WMF على بيانات EMF مضمنة. يستخدم برنامج MS Word في معظم الحالات بيانات EMF المضمنة. يستخدم GDI+ دائمًا بيانات WMF.

عندما يتم ضبط هذه القيمة على`حقيقي`يستخدم Aspose.Words بيانات EMF المضمنة عند العرض.

عندما يتم ضبط هذه القيمة على`خطأ شنيع`يستخدم Aspose.Words بيانات WMF عند العرض.

يتم استخدام هذا الخيار فقط عندما يتم عرض ملف التعريف كرسومات متجهة. عندما يتم تقديم ملف التعريف إلى صورة نقطية، يتم استخدام بيانات WMF دائمًا.

القيمة الافتراضية هي`حقيقي`.

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

* class [MetafileRenderingOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../metafilerenderingoptions/)
* المجسم [Aspose.Words](../../../)


