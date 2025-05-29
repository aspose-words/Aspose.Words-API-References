---
title: ShapeBase.BoundsWithEffects
linktitle: BoundsWithEffects
articleTitle: BoundsWithEffects
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase BoundsWithEffects للحصول على المدى النهائي لشكلتك بعد تطبيق تأثيرات الرسم، والتي يتم قياسها بالنقاط من أجل الدقة.
type: docs
weight: 90
url: /ar/net/aspose.words.drawing/shapebase/boundswitheffects/
---
## ShapeBase.BoundsWithEffects property

يحصل على المدى النهائي الذي أصبح عليه كائن الشكل هذا بعد تطبيق تأثيرات الرسم. يتم قياس القيمة بالنقاط.

```csharp
public RectangleF BoundsWithEffects { get; }
```

## أمثلة

يوضح كيفية التحقق من كيفية تأثر حدود الشكل بتأثيرات الشكل.

```csharp
Document doc = new Document(MyDir + "Shape shadow effect.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

//الشكلان متماثلان من حيث الأبعاد ونوع الشكل.
Assert.AreEqual(shapes[0].Width, shapes[1].Width);
Assert.AreEqual(shapes[0].Height, shapes[1].Height);
Assert.AreEqual(shapes[0].ShapeType, shapes[1].ShapeType);

// الشكل الأول ليس له أي تأثيرات، والشكل الثاني له ظل وخطوط عريضة سميكة.
//تؤدي هذه التأثيرات إلى جعل حجم الصورة الظلية للشكل الثاني أكبر من حجم الشكل الأول.
// على الرغم من أن حجم المستطيل يظهر عندما نضغط على هذه الأشكال في Microsoft Word،
// الحدود الخارجية المرئية للشكل الثاني تتأثر بالظل والمخطط التفصيلي وبالتالي تكون أكبر.
//يمكننا استخدام طريقة "AdjustWithEffects" لرؤية الحجم الحقيقي للشكل.
Assert.AreEqual(0.0, shapes[0].StrokeWeight);
Assert.AreEqual(20.0, shapes[1].StrokeWeight);
Assert.False(shapes[0].ShadowEnabled);
Assert.True(shapes[1].ShadowEnabled);

Shape shape = shapes[0];

// قم بإنشاء كائن RectangleF، الذي يمثل مستطيلًا،
// والتي يمكننا استخدامها كإحداثيات وحدود لشكل ما.
RectangleF rectangleF = new RectangleF(200, 200, 1000, 1000);

// قم بتشغيل هذه الطريقة للحصول على حجم المستطيل المعدل لجميع تأثيرات الشكل لدينا.
RectangleF rectangleFOut = shape.AdjustWithEffects(rectangleF);

// نظرًا لأن الشكل ليس له تأثيرات تغيير الحدود، فإن أبعاد حدوده لا تتأثر.
Assert.AreEqual(200, rectangleFOut.X);
Assert.AreEqual(200, rectangleFOut.Y);
Assert.AreEqual(1000, rectangleFOut.Width);
Assert.AreEqual(1000, rectangleFOut.Height);

// التحقق من المدى النهائي للشكل الأول، بالنقاط.
Assert.AreEqual(0, shape.BoundsWithEffects.X);
Assert.AreEqual(0, shape.BoundsWithEffects.Y);
Assert.AreEqual(147, shape.BoundsWithEffects.Width);
Assert.AreEqual(147, shape.BoundsWithEffects.Height);

shape = shapes[1];
rectangleF = new RectangleF(200, 200, 1000, 1000);
rectangleFOut = shape.AdjustWithEffects(rectangleF);

// لقد حركت تأثيرات الشكل الزاوية العلوية اليسرى الظاهرة للشكل قليلاً.
Assert.AreEqual(171.5, rectangleFOut.X);
Assert.AreEqual(167, rectangleFOut.Y);

// لقد أثرت التأثيرات أيضًا على الأبعاد المرئية للشكل.
Assert.AreEqual(1045, rectangleFOut.Width);
Assert.AreEqual(1133.5, rectangleFOut.Height);

// لقد أثرت التأثيرات أيضًا على الحدود المرئية للشكل.
Assert.AreEqual(-28.5, shape.BoundsWithEffects.X);
Assert.AreEqual(-33, shape.BoundsWithEffects.Y);
Assert.AreEqual(192, shape.BoundsWithEffects.Width);
Assert.AreEqual(280.5, shape.BoundsWithEffects.Height);
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
