---
title: SaveOptions.DmlRenderingMode
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية SaveOptions DmlRenderingMode عرض الأشكال في DrawingML. حسّن صور مستندك بسهولة!
type: docs
weight: 70
url: /ar/net/aspose.words.saving/saveoptions/dmlrenderingmode/
---
## SaveOptions.DmlRenderingMode property

يحصل على قيمة تحدد كيفية عرض أشكال DrawingML أو يعينها.

```csharp
public DmlRenderingMode DmlRenderingMode { get; set; }
```

## ملاحظات

القيمة الافتراضية هيFallback .

يتم استخدام هذه الخاصية عند تصدير المستند إلى تنسيقات الصفحات الثابتة.

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

* enum [DmlRenderingMode](../../dmlrenderingmode/)
* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
