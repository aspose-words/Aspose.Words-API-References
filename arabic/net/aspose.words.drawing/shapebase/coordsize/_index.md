---
title: ShapeBase.CoordSize
linktitle: CoordSize
articleTitle: CoordSize
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase CoordSize، التي تحدد عرض وارتفاع مساحة الإحداثيات للتحكم الأمثل في التخطيط في مشاريع التصميم الخاصة بك.
type: docs
weight: 120
url: /ar/net/aspose.words.drawing/shapebase/coordsize/
---
## ShapeBase.CoordSize property

عرض وارتفاع مساحة الإحداثيات داخل الكتلة التي تحتوي على هذا الشكل.

```csharp
public Size CoordSize { get; set; }
```

## ملاحظات

القيمة الافتراضية هي (1000، 1000).

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

يوضح كيفية إنشاء شكل المجموعة وتعبئته.

```csharp
Document doc = new Document();

// أنشئ شكلًا جماعيًا. يمكن لشكل المجموعة عرض مجموعة من عقد الأشكال الفرعية.
// في Microsoft Word، سيؤدي النقر داخل حدود شكل المجموعة أو على أحد الأشكال الفرعية لشكل المجموعة إلى
// حدد جميع الأشكال الفرعية الأخرى ضمن هذه المجموعة واسمح لنا بتغيير حجم جميع الأشكال وتحريكها مرة واحدة.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// قم بإنشاء شكل مجموعة بحجم 400 نقطة × 400 نقطة ووضعه في أصل إحداثيات الشكل العائم للمستند.
group.Bounds = new RectangleF(0, 0, 400, 400);

 // قم بتعيين حجم المستوى الإحداثي الداخلي للمجموعة إلى 500 × 500 نقطة.
// سيكون للزاوية العلوية اليسرى للمجموعة إحداثيات x و y (0، 0)،
// والزاوية اليمنى السفلية سيكون لها إحداثيات x و y (500، 500).
group.CoordSize = new Size(500, 500);

 // قم بتعيين إحداثيات الزاوية العلوية اليسرى للمجموعة إلى (-250، -250).
// سيكون لمركز المجموعة الآن قيمة إحداثيات x و y (0، 0)،
//وسوف تكون الزاوية اليمنى السفلية عند (250، 250).
group.CoordOrigin = new Point(-250, -250);

// قم بإنشاء مستطيل يعرض حدود شكل المجموعة هذا وإضافته إلى المجموعة.
Shape child1 = new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
};
group.AppendChild(child1);

// بمجرد أن يصبح الشكل جزءًا من مجموعة أشكال، يمكننا الوصول إليه كعقدة فرعية ثم تعديله.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// قم بإنشاء نجمة حمراء صغيرة وأدخلها في المجموعة.
// قم بمحاذاة الشكل مع أصل إحداثيات المجموعة، والتي قمنا بنقلها إلى المركز.
Shape child2 = new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
};
group.AppendChild(child2);

// قم بإدراج مستطيل، ثم قم بإدراج مستطيل أصغر قليلاً في نفس المكان مع الصورة.
// الأشكال الأحدث التي نضيفها إلى المجموعة تتداخل مع الأشكال القديمة. المستطيل الأزرق الفاتح سيتداخل جزئيًا مع النجمة الحمراء.
// ثم سيتداخل الشكل مع الصورة مع المستطيل الأزرق الفاتح، واستخدامه كإطار.
// لا يمكننا استخدام خصائص "ZOrder" الخاصة بالأشكال للتلاعب بترتيبها داخل شكل المجموعة.
Shape child3 = new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
};
group.AppendChild(child3);

Shape child4 = new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
};
group.AppendChild(child4);

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// أدخل مربع نص في شكل المجموعة. اضبط خاصية "يسار" بحيث تكون الحافة اليمنى لمربع النص
// يلامس الحد الأيمن لشكل المجموعة. اضبط خاصية "الأعلى" بحيث يكون مربع النص خارجها.
// حدود شكل المجموعة، مع حجمها العلوي المصطف على طول الهامش السفلي لشكل المجموعة.
Shape child5 = new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
};
group.AppendChild(child5);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(group);
builder.MoveTo(((Shape)group.GetChild(NodeType.Shape, 4, true)).AppendChild(new Paragraph(doc)));
builder.Write("Hello world!");

doc.Save(ArtifactsDir + "Shape.GroupShape.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
