---
title: TwoColorGradient
second_title: Aspose.Words لمراجع .NET API
description: يضبط التعبئة المحددة لتدرج لوني ثنائي اللون.
type: docs
weight: 210
url: /ar/net/aspose.words.drawing/fill/twocolorgradient/
---
## TwoColorGradient(GradientStyle, GradientVariant) {#twocolorgradient}

يضبط التعبئة المحددة لتدرج لوني ثنائي اللون.

```csharp
public void TwoColorGradient(GradientStyle style, GradientVariant variant)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| style | GradientStyle | أسلوب التدرج[`GradientStyle`](../../gradientstyle/). |
| variant | GradientVariant | متغير التدرج[`GradientVariant`](../../gradientvariant/) |

### أمثلة

يوضح كيفية تعبئة شكل بتدرجات لونية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// قم بتطبيق تعبئة متدرجة بلون واحد على الشكل باستخدام لون تعبئة متدرج.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// تطبيق تعبئة متدرجة ثنائية اللون على الشكل.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// تغيير لون الخلفية للتعبئة المتدرجة.
shape.Fill.BackColor = Color.Yellow;
// لاحظ أن التغييرات "GradientAngle" إلى "GradientStyle.FromCorner / GradientStyle.FromCenter"
// لا تحصل التعبئة المتدرجة على أي تأثير ، وستعمل فقط مع التدرج الخطي.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// استخدم خيار التوافق لتحديد الشكل باستخدام DML إذا كنت تريد الحصول على "GradientStyle" ،
// خصائص "GradientVariant" و "GradientAngle" بعد حفظ المستند.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### أنظر أيضا

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../fill/)
* المجسم [Aspose.Words](../../../)

---

## TwoColorGradient(Color, Color, GradientStyle, GradientVariant) {#twocolorgradient_1}

يضبط التعبئة المحددة لتدرج لوني ثنائي اللون.

```csharp
public void TwoColorGradient(Color color1, Color color2, GradientStyle style, 
    GradientVariant variant)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| color1 | Color | أول لون لبناء التدرج. |
| color2 | Color | اللون الثاني لبناء التدرج. |
| style | GradientStyle | أسلوب التدرج[`GradientStyle`](../../gradientstyle/). |
| variant | GradientVariant | متغير التدرج[`GradientVariant`](../../gradientvariant/) |

### أمثلة

يوضح كيفية تعبئة شكل بتدرجات لونية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// قم بتطبيق تعبئة متدرجة بلون واحد على الشكل باستخدام لون تعبئة متدرج.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// تطبيق تعبئة متدرجة ثنائية اللون على الشكل.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// تغيير لون الخلفية للتعبئة المتدرجة.
shape.Fill.BackColor = Color.Yellow;
// لاحظ أن التغييرات "GradientAngle" إلى "GradientStyle.FromCorner / GradientStyle.FromCenter"
// لا تحصل التعبئة المتدرجة على أي تأثير ، وستعمل فقط مع التدرج الخطي.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// استخدم خيار التوافق لتحديد الشكل باستخدام DML إذا كنت تريد الحصول على "GradientStyle" ،
// خصائص "GradientVariant" و "GradientAngle" بعد حفظ المستند.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### أنظر أيضا

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../fill/)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
