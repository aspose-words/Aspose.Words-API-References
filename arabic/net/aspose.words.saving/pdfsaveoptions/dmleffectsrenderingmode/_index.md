---
title: PdfSaveOptions.DmlEffectsRenderingMode
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. الحصول على أو تعيين قيمة تحدد كيفية عرض تأثيرات DrawingML .
type: docs
weight: 80
url: /ar/net/aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/
---
## PdfSaveOptions.DmlEffectsRenderingMode property

الحصول على أو تعيين قيمة تحدد كيفية عرض تأثيرات DrawingML .

```csharp
public override DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

### ملاحظات

القيمة الافتراضية هيSimplified .

يتم استخدام هذه الخاصية عند تصدير الوثيقة إلى تنسيقات الصفحات الثابتة.

إذا[`Compliance`](../compliance/) تم تعيينه علىPdfA1a أوPdfA1b ، الخاصية تُرجع دائمًاNone.

### أمثلة

يوضح كيفية تكوين جودة العرض لتأثيرات DrawingML في مستند أثناء حفظه في PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions options = new PdfSaveOptions();

// قم بتعيين خاصية "DmlEffectsRenderingMode" على "DmlEffectsRenderingMode.None" لتجاهل كافة تأثيرات DrawingML.
// تعيين خاصية "DmlEffectsRenderingMode" على "DmlEffectsRenderingMode.Simplified"
// لتقديم نسخة مبسطة من تأثيرات DrawingML.
// قم بتعيين خاصية "DmlEffectsRenderingMode" على "DmlEffectsRenderingMode.Fine" إلى
// تقديم تأثيرات DrawingML بمزيد من الدقة وأيضًا بتكلفة معالجة أكبر.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### أنظر أيضا

* enum [DmlEffectsRenderingMode](../../dmleffectsrenderingmode/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


