---
title: DmlEffectsRenderingMode Enum
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words لـ .NET
description: اكتشف وضع DmlEffectsRenderingMode في Aspose.Words لتحسين عرض تأثيرات DrawingML بتنسيقات صفحات ثابتة. حسّن جودة مستندك!
type: docs
weight: 5660
url: /ar/net/aspose.words.saving/dmleffectsrenderingmode/
---
## DmlEffectsRenderingMode enumeration

يحدد كيفية عرض تأثيرات DrawingML على تنسيقات الصفحات الثابتة.

```csharp
public enum DmlEffectsRenderingMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Simplified | `0` | تم تبسيط عرض تأثيرات DrawingML. |
| None | `1` | لا يتم عرض تأثيرات DrawingML. |
| Fine | `2` | يتم تقديم تأثيرات DrawingML في الوضع الدقيق الذي يتضمن معالجة متقدمة. في هذا الوضع، يعطي تقديم التأثيرات نتائج أفضل ولكن بتكلفة أداء أعلى منSimplified الوضع. |

## أمثلة

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
