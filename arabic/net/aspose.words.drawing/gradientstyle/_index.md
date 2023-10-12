---
title: Enum GradientStyle
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.GradientStyle تعداد. يحدد نمط التعبئة المتدرجة.
type: docs
weight: 1000
url: /ar/net/aspose.words.drawing/gradientstyle/
---
## GradientStyle enumeration

يحدد نمط التعبئة المتدرجة.

```csharp
public enum GradientStyle
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `-1` | لا يوجد تدرج. |
| Horizontal | `1` | التدرج الأفقي عبر الكائن. |
| Vertical | `2` | التدرج الذي يعمل عموديًا لأسفل الكائن. |
| DiagonalUp | `3` | التدرج القطري من الزاوية السفلية إلى الزاوية المقابلة. |
| DiagonalDown | `4` | التدرج القطري ينتقل من الزاوية العلوية للأسفل إلى الزاوية المقابلة. |
| FromCorner | `5` | التدرج من الزاوية إلى الزوايا الثلاث الأخرى. |
| FromCenter | `6` | التدرج يمتد من المركز إلى الزوايا. |

### أمثلة

يوضح كيفية تعبئة الشكل بالتدرجات اللونية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// قم بتطبيق تعبئة متدرجة أحادية اللون على الشكل باستخدام ForeColor للتعبئة المتدرجة.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// قم بتطبيق تعبئة متدرجة بلونين على الشكل.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// تغيير اللون الخلفي للتعبئة المتدرجة.
shape.Fill.BackColor = Color.Yellow;
// لاحظ أن التغييرات "GradientAngle" لـ "GradientStyle.FromCorner/GradientStyle.FromCenter"
// التعبئة المتدرجة لا تحصل على أي تأثير، فهي ستعمل فقط مع التدرج الخطي.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// استخدم خيار الامتثال لتحديد الشكل باستخدام DML إذا كنت تريد الحصول على "GradientStyle"،
// خصائص "GradientVariant" و"GradientAngle" بعد حفظ المستند.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)


