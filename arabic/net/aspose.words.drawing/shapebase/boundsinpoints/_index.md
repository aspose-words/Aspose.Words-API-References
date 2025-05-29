---
title: ShapeBase.BoundsInPoints
linktitle: BoundsInPoints
articleTitle: BoundsInPoints
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase BoundsInPoints للوصول بسهولة إلى حجم الشكل وموقعه بالنقاط، مما يعزز دقة التصميم والتحكم في التخطيط.
type: docs
weight: 80
url: /ar/net/aspose.words.drawing/shapebase/boundsinpoints/
---
## ShapeBase.BoundsInPoints property

يحصل على موقع وحجم الكتلة التي تحتوي على الشكل بالنقاط، بالنسبة لمرساة الشكل الأعلى.

```csharp
public RectangleF BoundsInPoints { get; }
```

## ملاحظات

لا تتضمن الحدود المرتجعة دوران هذا الشكل أو دوران شكل المجموعة الأصلية، إن وجد.

## أمثلة

يوضح كيفية التحقق من الشكل الذي يحتوي على حدود الكتلة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// على الرغم من أن السطر نفسه يشغل مساحة صغيرة على صفحة المستند،
// إنه يشغل كتلة مستطيلة الشكل، ويمكننا تحديد حجمها باستخدام خصائص "الحدود".
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// قم بإنشاء شكل مجموعة، ثم قم بتعيين حجم الكتلة التي تحتويها باستخدام خاصية "الحدود".
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// قم بإنشاء مستطيل، ثم تحقق من حجم الكتلة المحيطة به، ثم أضفه إلى شكل المجموعة.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// يقع أصل المستوى الإحداثي لشكل المجموعة في الزاوية العلوية اليسرى من الكتلة التي تحتويها،
// وإحداثيات x و y لـ (1000، 1000) في الزاوية اليمنى السفلية.
// حجم شكل مجموعتنا هو 250 × 250 نقطة، لذا فإن كل 4 نقاط على المستوى الإحداثي لشكل المجموعة
// يترجم إلى 1 نقطة في المستوى الإحداثي لنص المستند.
// كل شكل نقوم بإدراجه سوف يتقلص حجمه أيضًا بعامل 4.
// سينعكس هذا التغيير في خاصية "BoundsInPoints" الخاصة بالشكل.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// أدخل شكلاً ثم ضعه خارج حدود الكتلة التي تحتوي على الشكل الجماعي.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// لقد زادت مساحة شكل المجموعة في نص المستند، ولكن الكتلة التي تحتوي عليها ظلت كما هي.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
