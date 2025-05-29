---
title: GradientStop Class
linktitle: GradientStop
articleTitle: GradientStop
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.GradientStop، الحل الخاص بك لإنشاء تدرجات مذهلة مع توقفات قابلة للتخصيص لتحسين المرئيات في المستندات.
type: docs
weight: 1310
url: /ar/net/aspose.words.drawing/gradientstop/
---
## GradientStop class

يمثل نقطة توقف واحدة للتدرج.

لمعرفة المزيد، قم بزيارة[العمل مع العناصر الرسومية](https://docs.aspose.com/words/net/working-with-graphic-elements/) مقالة توثيقية.

```csharp
public class GradientStop
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [GradientStop](gradientstop/#constructor)(*Color, double*) | يقوم بتهيئة مثيل جديد لـ`GradientStop` الصف. |
| [GradientStop](gradientstop/#constructor_1)(*Color, double, double*) | يقوم بتهيئة مثيل جديد لـ`GradientStop` الصف. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BaseColor](../../aspose.words.drawing/gradientstop/basecolor/) { get; } | يحصل على قيمة تمثل لون توقف التدرج اللوني بدون أي تعديلات. |
| [Color](../../aspose.words.drawing/gradientstop/color/) { get; set; } | يحصل على قيمة تمثل لون توقف التدرج أو يعينها. |
| [Position](../../aspose.words.drawing/gradientstop/position/) { get; set; } | يحصل على قيمة تمثل موضع التوقف ضمن gradient معبرًا عنها كنسبة مئوية في النطاق من 0.0 إلى 1.0 أو يعينها. |
| [Transparency](../../aspose.words.drawing/gradientstop/transparency/) { get; set; } | يحصل على قيمة تمثل شفافية تعبئة التدرج أو يعينها، معبرًا عنها كنسبة مئوية في نطاق من 0.0 إلى 1.0. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Remove](../../aspose.words.drawing/gradientstop/remove/)() | يزيل توقف التدرج من الأصل[`GradientStopCollection`](../gradientstopcollection/) . |

## أمثلة

يوضح كيفية إضافة توقفات التدرج إلى التعبئة المتدرجة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// الحصول على مجموعة توقفات التدرج.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

//تغيير أول نقطة توقف للتدرج.
gradientStops[0].Color = Color.Aqua;
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

//أضف نقطة توقف تدرجية جديدة إلى نهاية المجموعة.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// قم بإزالة توقف التدرج عند الفهرس 1.
gradientStops.RemoveAt(1);
// وأدخل نقطة توقف تدرجية جديدة عند نفس الفهرس 1.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// قم بإزالة آخر نقطة توقف للتدرج في المجموعة.
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

// استخدم خيار التوافق لتحديد الشكل باستخدام DML
// إذا كنت تريد الحصول على خاصية "GradientStops" بعد حفظ المستند.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
