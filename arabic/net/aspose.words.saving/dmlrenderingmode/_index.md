---
title: DmlRenderingMode Enum
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يُحسّن وضع Aspose.Words.Saving.DmlRenderingMode عرض الأشكال في DrawingML للحصول على تنسيقات صفحات ثابتة عالية الجودة. حسّن صور مستنداتك!
type: docs
weight: 5670
url: /ar/net/aspose.words.saving/dmlrenderingmode/
---
## DmlRenderingMode enumeration

يحدد كيفية عرض أشكال DrawingML إلى تنسيقات الصفحة الثابتة.

```csharp
public enum DmlRenderingMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Fallback | `0` | إذا كان الشكل البديل متاحًا لـ DrawingML، يقوم Aspose.Words بعرض الشكل البديل بدلاً من DrawingML. |
| DrawingML | `1` | يتجاهل Aspose.Words الشكل البديل لـ DrawingML ويقوم بعرض DrawingML نفسه. هذا هو الوضع الافتراضي. |

## أمثلة

يوضح كيفية عرض الأشكال البديلة عند الحفظ في PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "DmlRenderingMode" إلى "DmlRenderingMode.Fallback"
// لاستبدال أشكال DML بأشكالها البديلة.
// اضبط خاصية "DmlRenderingMode" على "DmlRenderingMode.DrawingML"
//لتقديم أشكال DML نفسها.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

يوضح كيفية تكوين جودة عرض تأثيرات DrawingML في مستند أثناء حفظه في PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// قم بتعيين خاصية "DmlEffectsRenderingMode" إلى "DmlEffectsRenderingMode.None" لتجاهل جميع تأثيرات DrawingML.
// اضبط خاصية "DmlEffectsRenderingMode" إلى "DmlEffectsRenderingMode.Simplified"
// لتقديم نسخة مبسطة من تأثيرات DrawingML.
// اضبط خاصية "DmlEffectsRenderingMode" إلى "DmlEffectsRenderingMode.Fine" إلى
// تقديم تأثيرات DrawingML بدقة أكبر وبتكلفة معالجة أكبر.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
