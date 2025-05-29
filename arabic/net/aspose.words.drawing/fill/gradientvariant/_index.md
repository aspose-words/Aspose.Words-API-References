---
title: Fill.GradientVariant
linktitle: GradientVariant
articleTitle: GradientVariant
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية ضبط خاصية GradientVariant للحصول على تأثيرات تعبئة مذهلة. حسّن تصميمك بخيارات تدرج لوني نابضة بالحياة اليوم!
type: docs
weight: 130
url: /ar/net/aspose.words.drawing/fill/gradientvariant/
---
## Fill.GradientVariant property

يحصل على متغير التدرج[`GradientVariant`](../../gradientvariant/) للتعبئة.

```csharp
public GradientVariant GradientVariant { get; }
```

## أمثلة

يوضح كيفية ملء الشكل باستخدام التدرجات اللونية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// قم بتطبيق تعبئة التدرج اللوني أحادية اللون على الشكل باستخدام ForeColor للتعبئة التدرجية.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// قم بتطبيق تعبئة التدرج اللوني ثنائي اللون على الشكل.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// تغيير اللون الخلفي للتعبئة المتدرجة.
shape.Fill.BackColor = Color.Yellow;
// لاحظ أن التغييرات "GradientAngle" لـ "GradientStyle.FromCorner/GradientStyle.FromCenter"
// لا يحصل ملء التدرج على أي تأثير، وسوف يعمل فقط للتدرج الخطي.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// استخدم خيار التوافق لتحديد الشكل باستخدام DML إذا كنت تريد الحصول على "GradientStyle"،
// خصائص "GradientVariant" و"GradientAngle" بعد حفظ المستند.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### أنظر أيضا

* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
