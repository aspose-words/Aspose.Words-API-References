---
title: SaveOptions.DmlRenderingMode
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: Aspose.Words لـ .NET
description: SaveOptions DmlRenderingMode ملكية. الحصول على قيمة أو تعيينها لتحديد كيفية عرض أشكال DrawML في C#.
type: docs
weight: 70
url: /ar/net/aspose.words.saving/saveoptions/dmlrenderingmode/
---
## SaveOptions.DmlRenderingMode property

الحصول على قيمة أو تعيينها لتحديد كيفية عرض أشكال DrawML.

```csharp
public DmlRenderingMode DmlRenderingMode { get; set; }
```

## ملاحظات

القيمة الافتراضية هيFallback .

يتم استخدام هذه الخاصية عند تصدير المستند إلى تنسيقات صفحات ثابتة.

## أمثلة

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

* enum [DmlRenderingMode](../../dmlrenderingmode/)
* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
