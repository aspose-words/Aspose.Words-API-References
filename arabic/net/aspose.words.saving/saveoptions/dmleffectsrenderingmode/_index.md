---
title: SaveOptions.DmlEffectsRenderingMode
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words لـ .NET
description: SaveOptions DmlEffectsRenderingMode ملكية. الحصول على قيمة أو تعيينها لتحديد كيفية عرض تأثيرات DrawML في C#.
type: docs
weight: 60
url: /ar/net/aspose.words.saving/saveoptions/dmleffectsrenderingmode/
---
## SaveOptions.DmlEffectsRenderingMode property

الحصول على قيمة أو تعيينها لتحديد كيفية عرض تأثيرات DrawML.

```csharp
public virtual DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

## ملاحظات

القيمة الافتراضية هيSimplified .

يتم استخدام هذه الخاصية عند تصدير المستند إلى تنسيقات صفحات ثابتة.

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

* enum [DmlEffectsRenderingMode](../../dmleffectsrenderingmode/)
* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
