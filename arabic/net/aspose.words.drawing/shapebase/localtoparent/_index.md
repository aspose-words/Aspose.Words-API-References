---
title: ShapeBase.LocalToParent
linktitle: LocalToParent
articleTitle: LocalToParent
second_title: Aspose.Words لـ .NET
description: حوّل الإحداثيات المحلية إلى مساحة شكل رئيسية باستخدام طريقة ShapeBase LocalToParent. حسّن دقة مشاريع النمذجة ثلاثية الأبعاد الخاصة بك اليوم!
type: docs
weight: 680
url: /ar/net/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase.LocalToParent method

يحول قيمة من مساحة الإحداثيات المحلية إلى مساحة الإحداثيات للشكل الأصلي.

```csharp
public PointF LocalToParent(PointF value)
```

## أمثلة

يوضح كيفية ترجمة موقع إحداثيات x وy على المستوى الإحداثي للشكل إلى موقع على المستوى الإحداثي للشكل الأصلي.

```csharp
Document doc = new Document();

// أدخل شكل المجموعة، ثم ضعه على بعد 100 نقطة أسفل وإلى يمين
// نقطة أصل إحداثيات x وy للمستند.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// استخدم طريقة "LocalToParent" لتحديد أن (0، 0) على إحداثيات x و y الداخلية للمجموعة
// يقع على (100، 100) من نظام إحداثيات الشكل الرئيسي. الشكل الرئيسي للمجموعة هو المستند نفسه.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// بشكل افتراضي، يكون مستوى الإحداثيات الداخلية للشكل في الزاوية العلوية اليسرى عند (0، 0)،
// والزاوية اليمنى السفلية عند (1000، 1000). نظرًا لحجمها، يغطي شكل مجموعتنا مساحة 500 نقطة × 500 نقطة.
// في مستوى المستند. هذا يعني أن أي حركة بمقدار نقطة واحدة على مستوى إحداثيات المستند ستُترجم
// إلى حركة بمقدار 2 نقطة على المستوى الإحداثي لشكل المجموعة.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// نقل أصل المحورين x وy لشكل المجموعة من الزاوية العلوية اليسرى إلى المركز.
// سيؤدي هذا إلى إزاحة إحداثيات المجموعة الداخلية بالنسبة إلى إحداثيات المستند بشكل أكبر.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// سيؤدي تغيير مقياس المستوى الإحداثي أيضًا إلى التأثير على المواقع النسبية.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// إذا أردنا إضافة شكل إلى هذه المجموعة أثناء تحديد موقعه استنادًا إلى موقع في المستند،
// سوف نحتاج أولاً إلى تأكيد الموقع في شكل المجموعة الذي سيتطابق مع موقع المستند.
Assert.AreEqual(new PointF(700, 700), group.LocalToParent(new PointF(350, 350)));

Shape shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

group.AppendChild(shape);
doc.FirstSection.Body.FirstParagraph.AppendChild(group);

doc.Save(ArtifactsDir + "Shape.LocalToParent.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
