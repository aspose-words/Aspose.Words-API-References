---
title: SaveOptions.DmlEffectsRenderingMode
second_title: Aspose.Words لمراجع .NET API
description: SaveOptions ملكية. الحصول على أو تعيين قيمة تحدد كيفية عرض تأثيرات DrawingML .
type: docs
weight: 60
url: /ar/net/aspose.words.saving/saveoptions/dmleffectsrenderingmode/
---
## SaveOptions.DmlEffectsRenderingMode property

الحصول على أو تعيين قيمة تحدد كيفية عرض تأثيرات DrawingML .

```csharp
public virtual DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

### ملاحظات

القيمة الافتراضية هيSimplified .

يتم استخدام هذه الخاصية عند تصدير الوثيقة إلى تنسيقات الصفحات الثابتة.

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
* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../saveoptions/)
* المجسم [Aspose.Words](../../../)


