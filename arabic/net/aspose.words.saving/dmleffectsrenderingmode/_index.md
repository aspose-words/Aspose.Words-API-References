---
title: DmlEffectsRenderingMode Enum
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.DmlEffectsRenderingMode تعداد. يحدد كيفية عرض تأثيرات DrawML إلى تنسيقات الصفحات الثابتة في C#.
type: docs
weight: 4910
url: /ar/net/aspose.words.saving/dmleffectsrenderingmode/
---
## DmlEffectsRenderingMode enumeration

يحدد كيفية عرض تأثيرات DrawML إلى تنسيقات الصفحات الثابتة.

```csharp
public enum DmlEffectsRenderingMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Simplified | `0` | تم تبسيط عرض تأثيرات DrawML. |
| None | `1` | لم يتم عرض تأثيرات DrawML. |
| Fine | `2` | يتم عرض تأثيرات DrawML في الوضع الدقيق الذي يتضمن معالجة متقدمة. في هذا الوضع، يؤدي عرض التأثيرات إلى نتائج أفضل ولكن بتكلفة أداء أعلى منSimplified الوضع. |

## أمثلة

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
