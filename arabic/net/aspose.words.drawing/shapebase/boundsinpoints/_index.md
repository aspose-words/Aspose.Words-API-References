---
title: ShapeBase.BoundsInPoints
linktitle: BoundsInPoints
articleTitle: BoundsInPoints
second_title: Aspose.Words لـ .NET
description: ShapeBase BoundsInPoints ملكية. الحصول على موقع وحجم الكتلة التي تحتوي على الشكل بالنقاط بالنسبة إلى نقطة ارتساء الشكل العلوي في C#.
type: docs
weight: 80
url: /ar/net/aspose.words.drawing/shapebase/boundsinpoints/
---
## ShapeBase.BoundsInPoints property

الحصول على موقع وحجم الكتلة التي تحتوي على الشكل بالنقاط، بالنسبة إلى نقطة ارتساء الشكل العلوي.

```csharp
public RectangleF BoundsInPoints { get; }
```

## أمثلة

يوضح كيفية التحقق من الشكل الذي يحتوي على حدود الكتلة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// على الرغم من أن السطر نفسه يشغل مساحة صغيرة على صفحة المستند،
// تشغل كتلة تحتوي على مستطيل، يمكننا تحديد حجمها باستخدام خصائص "الحدود".
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// قم بإنشاء شكل مجموعة، ثم قم بتعيين حجم الكتلة التي تحتوي عليه باستخدام خاصية "الحدود".
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// أنشئ مستطيلاً، وتحقق من حجم الكتلة المحيطة به، ثم أضفه إلى شكل المجموعة.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// يقع المستوى الإحداثي لشكل المجموعة في الزاوية العلوية اليسرى من الكتلة التي تحتوي عليه،
// وإحداثيات x وy (1000، 1000) في الزاوية اليمنى السفلية.
// حجم شكل مجموعتنا هو 250 × 250 نقطة، لذا فإن كل 4 نقاط على المستوى الإحداثي لشكل المجموعة
// يُترجم إلى 1pt في المستوى الإحداثي لنص الوثيقة.
// كل شكل نقوم بإدراجه سوف يتقلص حجمه أيضًا بعامل قدره 4.
// التغيير في خاصية "BoundsInPoints" للشكل سوف يعكس ذلك.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// قم بإدراج شكل ووضعه خارج حدود الكتلة التي تحتوي على شكل المجموعة.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// زاد حجم شكل المجموعة في نص المستند، لكن الكتلة التي تحتوي عليه تظل كما هي.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
