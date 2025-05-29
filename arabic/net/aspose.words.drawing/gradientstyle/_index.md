---
title: GradientStyle Enum
linktitle: GradientStyle
articleTitle: GradientStyle
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Drawing.GradientStyle للحصول على أنماط تعبئة متدرجة قابلة للتخصيص، مما يعزز تصميمات المستندات الخاصة بك باستخدام صور نابضة بالحياة.
type: docs
weight: 1330
url: /ar/net/aspose.words.drawing/gradientstyle/
---
## GradientStyle enumeration

يحدد النمط لتعبئة التدرج.

```csharp
public enum GradientStyle
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `-1` | لا يوجد تدرج. |
| Horizontal | `1` | تدرج لوني أفقيًا عبر كائن. |
| Vertical | `2` | تدرج لوني ينحدر عموديًا لأسفل أحد الكائنات. |
| DiagonalUp | `3` | تدرج قطري يتحرك من الزاوية السفلية إلى الزاوية المقابلة. |
| DiagonalDown | `4` | تدرج قطري يتحرك من الزاوية العلوية إلى الزاوية المقابلة. |
| FromCorner | `5` | تدرج لوني يمتد من زاوية إلى الزوايا الثلاث الأخرى. |
| FromCenter | `6` | تدرج لوني يمتد من المركز إلى الزوايا. |

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

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
