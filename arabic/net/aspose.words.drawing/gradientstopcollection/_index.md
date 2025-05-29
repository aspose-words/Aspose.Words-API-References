---
title: GradientStopCollection Class
linktitle: GradientStopCollection
articleTitle: GradientStopCollection
second_title: Aspose.Words لـ .NET
description: استكشف فئة Aspose.Words.Drawing.GradientStopCollection، التي تتميز بمجموعة قوية من كائنات GradientStop القابلة للتخصيص لتحسين تصميم المستندات.
type: docs
weight: 1320
url: /ar/net/aspose.words.drawing/gradientstopcollection/
---
## GradientStopCollection class

يحتوي على مجموعة من[`GradientStop`](../gradientstop/) الأشياء.

لمعرفة المزيد، قم بزيارة[العمل مع العناصر الرسومية](https://docs.aspose.com/words/net/working-with-graphic-elements/) مقالة توثيقية.

```csharp
public class GradientStopCollection : IEnumerable<GradientStop>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.drawing/gradientstopcollection/count/) { get; } | يحصل على قيمة عددية تشير إلى عدد العناصر في المجموعة. |
| [Item](../../aspose.words.drawing/gradientstopcollection/item/) { get; set; } | يحصل على أو يعين[`GradientStop`](../gradientstop/) الكائن في المجموعة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.drawing/gradientstopcollection/add/)(*[GradientStop](../gradientstop/)*) | يضيف محددًا[`GradientStop`](../gradientstop/) إلى التدرج. |
| [GetEnumerator](../../aspose.words.drawing/gradientstopcollection/getenumerator/)() | يعيد مُعَدِّدًا يتكرر خلال المجموعة. |
| [Insert](../../aspose.words.drawing/gradientstopcollection/insert/)(*int, [GradientStop](../gradientstop/)*) | يُدرج[`GradientStop`](../gradientstop/) إلى المجموعة عند فهرس محدد. |
| [Remove](../../aspose.words.drawing/gradientstopcollection/remove/)(*[GradientStop](../gradientstop/)*) | يزيل محددًا[`GradientStop`](../gradientstop/) من المجموعة. |
| [RemoveAt](../../aspose.words.drawing/gradientstopcollection/removeat/)(*int*) | يزيل[`GradientStop`](../gradientstop/) من المجموعة الموجودة في فهرس محدد. |

## ملاحظات

لا يمكنك إنشاء مثيلات لهذه الفئة بشكل مباشر. استخدم[`GradientStops`](../fill/gradientstops/) خاصية للوصول إلى توقفات التدرج لكائنات التعبئة.

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

* class [GradientStop](../gradientstop/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
