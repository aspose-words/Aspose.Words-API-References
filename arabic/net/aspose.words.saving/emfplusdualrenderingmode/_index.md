---
title: EmfPlusDualRenderingMode Enum
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words لـ .NET
description: اكتشف وضع العرض المزدوج EMF Plus من Aspose.Words لعرض مثالي لملفات التعريف EMF Dual. حسّن معالجة مستنداتك بدقة!
type: docs
weight: 5730
url: /ar/net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

يحدد كيفية قيام Aspose.Words بعرض ملفات التعريف EMF+ Dual.

```csharp
public enum EmfPlusDualRenderingMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | يحاول Aspose.Words عرض جزء من ملف EMF+ Dual. إذا لم تكن بعض سجلات EMF+ مدعومة، فسيعرض Aspose.Words جزء من ملف EMF+ Dual. |
| EmfPlus | `1` | Aspose.Words يعرض EMF+ كجزء من ملف التعريف المزدوج EMF+. |
| Emf | `2` | Aspose.Words يعرض جزء EMF من ملف التعريف المزدوج EMF+. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
