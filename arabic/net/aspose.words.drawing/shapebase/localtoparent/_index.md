---
title: ShapeBase.LocalToParent
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase طريقة. تحويل قيمة من المساحة الإحداثية المحلية إلى المساحة الإحداثية للشكل الأصلي.
type: docs
weight: 670
url: /ar/net/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase.LocalToParent method

تحويل قيمة من المساحة الإحداثية المحلية إلى المساحة الإحداثية للشكل الأصلي.

```csharp
public PointF LocalToParent(PointF value)
```

### أمثلة

يوضح كيفية ترجمة الموقع الإحداثي x وy على المستوى الإحداثي للشكل إلى موقع على المستوى الإحداثي للشكل الأصلي.

```csharp
Document doc = new Document();

// أدخل شكل المجموعة، وضعه 100 نقطة أدناه وعلى يمين
// نقطة الأصل الإحداثية x وY للمستند.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// استخدم طريقة "LocalToParent" لتحديد (0، 0) على إحداثيات x و y الداخلية للمجموعة
// يقع على (100، 100) من النظام الإحداثي للشكل الأصلي. أصل شكل المجموعة هو المستند نفسه.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// بشكل افتراضي، يكون مستوى الإحداثيات الداخلي للشكل في الزاوية اليسرى العليا عند (0، 0)،
// والزاوية اليمنى السفلية عند (1000، 1000). نظرًا لحجمها، فإن شكل مجموعتنا يغطي مساحة 500pt x 500pt
// في مستوى الوثيقة. وهذا يعني أنه سيتم ترجمة حركة مقدارها 1pt على المستوى الإحداثي للمستند
// لحركة بمقدار نقطتين على المستوى الإحداثي لشكل المجموعة.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// انقل أصل المحورين x وy لشكل المجموعة من الزاوية العلوية اليسرى إلى المركز.
// سيؤدي هذا إلى تعويض الإحداثيات الداخلية للمجموعة المتعلقة بإحداثيات المستند بشكل أكبر.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// سيؤثر تغيير مقياس المستوى الإحداثي أيضًا على المواقع النسبية.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// إذا أردنا إضافة شكل إلى هذه المجموعة أثناء تحديد موقعها بناءً على موقع في المستند،
// سنحتاج أولاً إلى تأكيد الموقع في شكل المجموعة الذي سيطابق موقع المستند.
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
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


