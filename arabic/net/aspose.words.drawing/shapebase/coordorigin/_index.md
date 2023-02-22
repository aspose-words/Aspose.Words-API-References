---
title: ShapeBase.CoordOrigin
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. الإحداثيات الموجودة في الزاوية العلوية اليسرى للكتلة التي تحتوي على هذا الشكل.
type: docs
weight: 110
url: /ar/net/aspose.words.drawing/shapebase/coordorigin/
---
## ShapeBase.CoordOrigin property

الإحداثيات الموجودة في الزاوية العلوية اليسرى للكتلة التي تحتوي على هذا الشكل.

```csharp
public Point CoordOrigin { get; set; }
```

### ملاحظات

القيمة الافتراضية هي (0،0).

### أمثلة

يوضح كيفية ترجمة موقع إحداثيات x و y على مستوى إحداثي الشكل إلى موقع على مستوى إحداثي الشكل الأصل.

```csharp
Document doc = new Document();

// أدخل شكل مجموعة ، وضعه 100 نقطة أسفل وعلى يمين
// نقطة أصل إحداثيات x و Y الخاصة بالمستند.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// استخدم طريقة "LocalToParent" لتحديد ذلك (0 ، 0) على إحداثيات x و y الداخلية للمجموعة
// تقع على (100 ، 100) من نظام إحداثيات الشكل الأصل. أصل شكل المجموعة هو المستند نفسه.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// بشكل افتراضي ، يكون مستوى الإحداثيات الداخلي للشكل أعلى الزاوية اليسرى عند (0 ، 0) ،
// والزاوية اليمنى السفلية عند (1000 ، 1000). نظرًا لحجمها ، فإن شكل مجموعتنا يغطي مساحة 500 نقطة × 500 نقطة
// في مستوى المستند. هذا يعني أنه سيتم ترجمة الحركة بمقدار 1 نقطة على مستوى إحداثي المستند
// لحركة 2 نقطة على مستوى إحداثيات شكل المجموعة.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// انقل أصل المحور x و y لشكل المجموعة من الزاوية اليسرى العلوية إلى المركز.
// سيؤدي ذلك إلى موازنة الإحداثيات الداخلية للمجموعة المتعلقة بإحداثيات المستند بشكل أكبر.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// سيؤثر تغيير مقياس مستوى الإحداثيات أيضًا على المواقع النسبية.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// إذا كنا نرغب في إضافة شكل إلى هذه المجموعة أثناء تحديد موقعها بناءً على موقع في المستند ،
// سنحتاج أولاً إلى تأكيد موقع في شكل المجموعة يتطابق مع موقع المستند.
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

يوضح كيفية إنشاء شكل مجموعة وملئه.

```csharp
Document doc = new Document();

// إنشاء شكل مجموعة. يمكن لشكل المجموعة أن يعرض مجموعة من عقد الشكل الفرعية.
// في Microsoft Word ، سيؤدي النقر داخل حدود شكل المجموعة أو على أحد الأشكال الفرعية لشكل المجموعة
// حدد جميع الأشكال الفرعية الأخرى داخل هذه المجموعة واسمح لنا بقياس وتحريك جميع الأشكال مرة واحدة.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// أنشئ شكل مجموعة 400pt x 400pt وضعه في أصل إحداثيات الشكل العائم للمستند.
group.Bounds = new RectangleF(0, 0, 400, 400);

 // اضبط حجم مستوى الإحداثي الداخلي للمجموعة على 500 × 500 نقطة.
// سيكون للزاوية اليسرى العلوية من المجموعة إحداثي x و y لـ (0 ، 0) ،
// والركن الأيمن السفلي سيكون له إحداثي x و y (500 ، 500).
group.CoordSize = new Size(500, 500);

 // اضبط إحداثيات الزاوية اليسرى العلوية للمجموعة على (-250 ، -250).
// سيحتوي مركز المجموعة الآن على قيمة إحداثي x و y تساوي (0 ، 0) ،
// والركن الأيمن السفلي سيكون (250 ، 250).
group.CoordOrigin = new Point(-250, -250);

// قم بإنشاء مستطيل يعرض حدود شكل المجموعة هذا وإضافته إلى المجموعة.
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
});

// بمجرد أن يصبح الشكل جزءًا من شكل مجموعة ، يمكننا الوصول إليه كعقدة فرعية ثم تعديله.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// أنشئ نجمة حمراء صغيرة وأدخلها في المجموعة.
// قم بمحاذاة الشكل مع أصل إحداثيات المجموعة ، والذي انتقلنا إليه إلى المركز.
group.AppendChild(new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
});

 // أدخل مستطيلاً ، ثم أدخل مستطيلاً أصغر قليلاً في نفس المكان مع الصورة.
// تتداخل الأشكال الأحدث التي نضيفها إلى المجموعة مع الأشكال الأقدم. سيتداخل المستطيل الأزرق الفاتح جزئيًا مع النجم الأحمر ،
// ثم يتداخل الشكل مع الصورة مع المستطيل الأزرق الفاتح ، باستخدامه كإطار.
 // لا يمكننا استخدام خصائص "ZOrder" للأشكال لمعالجة ترتيبها داخل شكل مجموعة.
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
});

group.AppendChild(new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
});

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// أدخل مربع نص في شكل المجموعة. قم بتعيين الخاصية "Left" بحيث تكون الحافة اليمنى لمربع النص
// يلامس الحد الأيمن لشكل المجموعة. عيّن الخاصية "Top" بحيث يقع مربع النص في الخارج
// حدود شكل المجموعة ، مع تحديد حجمها العلوي على طول الهامش السفلي لشكل المجموعة.
group.AppendChild(new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
});

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(group);
builder.MoveTo(((Shape)group.GetChild(NodeType.Shape, 4, true)).AppendChild(new Paragraph(doc)));
builder.Write("Hello world!");

doc.Save(ArtifactsDir + "Shape.GroupShape.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


