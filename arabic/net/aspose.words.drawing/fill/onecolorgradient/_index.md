---
title: Fill.OneColorGradient
second_title: Aspose.Words لمراجع .NET API
description: Fill طريقة. يضبط التعبئة المحددة على تدرج لوني واحد.
type: docs
weight: 220
url: /ar/net/aspose.words.drawing/fill/onecolorgradient/
---
## OneColorGradient(GradientStyle, GradientVariant, double) {#onecolorgradient}

يضبط التعبئة المحددة على تدرج لوني واحد.

```csharp
public void OneColorGradient(GradientStyle style, GradientVariant variant, double degree)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| style | GradientStyle | أسلوب التدرج[`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | البديل التدرج[`GradientVariant`](../../gradientvariant/) |
| degree | Double | درجة التدرج. يمكن أن تتراوح القيمة من 0.0 (داكن) إلى 1.0 (فاتح). |

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

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../fill/)
* المجسم [Aspose.Words](../../../)

---

## OneColorGradient(Color, GradientStyle, GradientVariant, double) {#onecolorgradient_1}

يضبط التعبئة المحددة على تدرج لوني واحد باستخدام اللون المحدد.

```csharp
public void OneColorGradient(Color color, GradientStyle style, GradientVariant variant, 
    double degree)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| color | Color | اللون لبناء التدرج. |
| style | GradientStyle | أسلوب التدرج[`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | البديل التدرج[`GradientVariant`](../../gradientvariant/) |
| degree | Double | درجة التدرج. يمكن أن تتراوح القيمة من 0.0 (داكن) إلى 1.0 (فاتح). |

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

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../fill/)
* المجسم [Aspose.Words](../../../)


