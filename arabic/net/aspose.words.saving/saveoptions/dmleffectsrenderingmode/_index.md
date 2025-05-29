---
title: SaveOptions.DmlEffectsRenderingMode
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية SaveOptions DmlEffectsRenderingMode على تحسين عرض تأثيرات DrawingML لتحسين جودة المستند والأداء.
type: docs
weight: 60
url: /ar/net/aspose.words.saving/saveoptions/dmleffectsrenderingmode/
---
## SaveOptions.DmlEffectsRenderingMode property

يحصل على قيمة تحدد كيفية عرض تأثيرات DrawingML أو يعينها.

```csharp
public virtual DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

## ملاحظات

القيمة الافتراضية هيSimplified .

يتم استخدام هذه الخاصية عند تصدير المستند إلى تنسيقات الصفحات الثابتة.

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

* enum [DmlEffectsRenderingMode](../../dmleffectsrenderingmode/)
* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
