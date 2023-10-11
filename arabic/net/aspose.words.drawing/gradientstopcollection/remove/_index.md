---
title: GradientStopCollection.Remove
second_title: Aspose.Words لمراجع .NET API
description: GradientStopCollection طريقة. يزيل المحددGradientStop من المجموعة.
type: docs
weight: 60
url: /ar/net/aspose.words.drawing/gradientstopcollection/remove/
---
## GradientStopCollection.Remove method

يزيل المحدد[`GradientStop`](../../gradientstop/) من المجموعة.

```csharp
public bool Remove(GradientStop gradientStop)
```

### قيمة الإرجاع

`حقيقي` إذا تمت إزالة توقف التدرج بنجاح، وإلا`خطأ شنيع`.

### أمثلة

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

* class [GradientStop](../../gradientstop/)
* class [GradientStopCollection](../)
* مساحة الاسم [Aspose.Words.Drawing](../../gradientstopcollection/)
* المجسم [Aspose.Words](../../../)


