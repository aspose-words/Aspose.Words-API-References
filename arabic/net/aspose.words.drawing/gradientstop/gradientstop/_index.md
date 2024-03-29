---
title: GradientStop
linktitle: GradientStop
articleTitle: GradientStop
second_title: Aspose.Words لـ .NET
description: GradientStop البناء. تهيئة مثيل جديد لـGradientStop فئة في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing/gradientstop/gradientstop/
---
## GradientStop(*Color, double*) {#constructor}

تهيئة مثيل جديد لـ[`GradientStop`](../) فئة.

```csharp
public GradientStop(Color color, double position)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| color | Color | يمثل لون توقف التدرج. |
| position | Double | يمثل موضع التوقف ضمن التدرج المعبر عنه كنسبة مئوية في النطاق من 0.0 إلى 1.0. |

## أمثلة

يوضح كيفية إضافة نقاط توقف متدرجة إلى التعبئة المتدرجة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// احصل على مجموعة توقفات التدرج.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// تغيير توقف التدرج الأول.            
gradientStops[0].Color = Color.Aqua;            
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// أضف نقطة توقف متدرجة جديدة إلى نهاية المجموعة.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// إزالة نقطة توقف التدرج عند الفهرس 1.
gradientStops.RemoveAt(1);
// وأدخل نقطة توقف متدرجة جديدة عند نفس الفهرس 1.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// قم بإزالة آخر نقطة توقف متدرجة في المجموعة.
gradientStop = gradientStops[2];
gradientStops.Remove(gradientStop);

Assert.AreEqual(2, gradientStops.Count);

Assert.AreEqual(Color.FromArgb(255, 0, 255, 255), gradientStops[0].BaseColor);
Assert.AreEqual(Color.Aqua.ToArgb(), gradientStops[0].Color.ToArgb());
Assert.AreEqual(0.1d, gradientStops[0].Position, 0.01d);
Assert.AreEqual(0.25d, gradientStops[0].Transparency, 0.01d);

Assert.AreEqual(Color.Chocolate.ToArgb(), gradientStops[1].Color.ToArgb());
Assert.AreEqual(0.75d, gradientStops[1].Position, 0.01d);
Assert.AreEqual(0.3d, gradientStops[1].Transparency, 0.01d);

// استخدم خيار الامتثال لتحديد الشكل باستخدام DML
// إذا كنت تريد الحصول على خاصية "GradientStops" بعد حفظ المستند.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### أنظر أيضا

* class [GradientStop](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)

---

## GradientStop(*Color, double, double*) {#constructor_1}

تهيئة مثيل جديد لـ[`GradientStop`](../) فئة.

```csharp
public GradientStop(Color color, double position, double transparency)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| color | Color | يمثل لون توقف التدرج. |
| position | Double | يمثل موضع التوقف ضمن التدرج المعبر عنه كنسبة مئوية في النطاق من 0.0 إلى 1.0. |
| transparency | Double | يمثل شفافية التوقف ضمن التدرج المعبر عنه كنسبة مئوية في النطاق من 0.0 إلى 1.0. |

## أمثلة

يوضح كيفية إضافة نقاط توقف متدرجة إلى التعبئة المتدرجة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// احصل على مجموعة توقفات التدرج.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// تغيير توقف التدرج الأول.            
gradientStops[0].Color = Color.Aqua;            
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// أضف نقطة توقف متدرجة جديدة إلى نهاية المجموعة.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// إزالة نقطة توقف التدرج عند الفهرس 1.
gradientStops.RemoveAt(1);
// وأدخل نقطة توقف متدرجة جديدة عند نفس الفهرس 1.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// قم بإزالة آخر نقطة توقف متدرجة في المجموعة.
gradientStop = gradientStops[2];
gradientStops.Remove(gradientStop);

Assert.AreEqual(2, gradientStops.Count);

Assert.AreEqual(Color.FromArgb(255, 0, 255, 255), gradientStops[0].BaseColor);
Assert.AreEqual(Color.Aqua.ToArgb(), gradientStops[0].Color.ToArgb());
Assert.AreEqual(0.1d, gradientStops[0].Position, 0.01d);
Assert.AreEqual(0.25d, gradientStops[0].Transparency, 0.01d);

Assert.AreEqual(Color.Chocolate.ToArgb(), gradientStops[1].Color.ToArgb());
Assert.AreEqual(0.75d, gradientStops[1].Position, 0.01d);
Assert.AreEqual(0.3d, gradientStops[1].Transparency, 0.01d);

// استخدم خيار الامتثال لتحديد الشكل باستخدام DML
// إذا كنت تريد الحصول على خاصية "GradientStops" بعد حفظ المستند.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### أنظر أيضا

* class [GradientStop](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
