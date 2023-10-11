---
title: Enum DmlRenderingMode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.DmlRenderingMode تعداد. يحدد كيفية عرض أشكال DrawML إلى تنسيقات الصفحات الثابتة.
type: docs
weight: 4920
url: /ar/net/aspose.words.saving/dmlrenderingmode/
---
## DmlRenderingMode enumeration

يحدد كيفية عرض أشكال DrawML إلى تنسيقات الصفحات الثابتة.

```csharp
public enum DmlRenderingMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Fallback | `0` | إذا كان الشكل الاحتياطي متاحًا لـ DrawML، فإن Aspose.Words يعرض الشكل الاحتياطي بدلاً من DrawML. |
| DrawingML | `1` | يتجاهل Aspose.Words الشكل الاحتياطي لـ DrawML ويعرض DrawML نفسه. هذا هو الوضع الافتراضي. |

### أمثلة

يوضح كيفية عرض الأشكال الاحتياطية عند الحفظ في ملف PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// قم بتعيين خاصية "DmlRenderingMode" على "DmlRenderingMode.Fallback"
// لاستبدال أشكال DML بأشكالها الاحتياطية.
// قم بتعيين خاصية "DmlRenderingMode" على "DmlRenderingMode.DrawingML"
// لتقديم أشكال DML نفسها.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

يوضح كيفية تكوين جودة العرض لتأثيرات DrawML في المستند أثناء حفظه في ملف PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// قم بتعيين خاصية "DmlEffectsRenderingMode" على "DmlEffectsRenderingMode.None" لتجاهل كافة تأثيرات DrawML.
// قم بتعيين خاصية "DmlEffectsRenderingMode" على "DmlEffectsRenderingMode.Simplified"
// لتقديم نسخة مبسطة من تأثيرات DrawML.
// قم بتعيين خاصية "DmlEffectsRenderingMode" على "DmlEffectsRenderingMode.Fine" إلى
// تقديم تأثيرات DrawML بدقة أكبر وبتكلفة معالجة أكبر أيضًا.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


