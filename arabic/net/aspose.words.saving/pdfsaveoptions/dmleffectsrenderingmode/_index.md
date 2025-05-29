---
title: PdfSaveOptions.DmlEffectsRenderingMode
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PdfSaveOptions DmlEffectsRenderingMode للتحكم في عرض تأثيرات DrawingML لتحسين جودة إخراج PDF.
type: docs
weight: 100
url: /ar/net/aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/
---
## PdfSaveOptions.DmlEffectsRenderingMode property

يحصل على قيمة تحدد كيفية عرض تأثيرات DrawingML أو يعينها.

```csharp
public override DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

## ملاحظات

القيمة الافتراضية هيSimplified .

يتم استخدام هذه الخاصية عند تصدير المستند إلى تنسيقات الصفحات الثابتة.

لو[`Compliance`](../compliance/) تم ضبطه علىPdfA1a أوPdfA1b , الخاصية ترجع دائمًاNone.

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
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
