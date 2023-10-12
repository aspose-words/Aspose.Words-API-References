---
title: Enum EmfPlusDualRenderingMode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.EmfPlusDualRenderingMode تعداد. يحدد كيفية عرض Aspose.Words لملفات تعريف EMF Dual.
type: docs
weight: 4980
url: /ar/net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

يحدد كيفية عرض Aspose.Words لملفات تعريف EMF+ Dual.

```csharp
public enum EmfPlusDualRenderingMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | يحاول Aspose.Words عرض EMF+ كجزء من ملف تعريف EMF+ Dual. إذا كانت بعض سجلات EMF+ غير مدعومة ، فسيعرض Aspose.Words جزءًا EMF من ملف تعريف EMF+ Dual. |
| EmfPlus | `1` | Aspose.Words يعرض EMF+ جزءًا من ملف تعريف EMF+ Dual. |
| Emf | `2` | Aspose.Words يعرض EMF جزءًا من ملف تعريف EMF+ Dual. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


