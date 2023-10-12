---
title: ShapeBase.CoordOrigin
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. الإحداثيات في الزاوية العلوية اليسرى للكتلة التي تحتوي على هذا الشكل.
type: docs
weight: 110
url: /ar/net/aspose.words.drawing/shapebase/coordorigin/
---
## ShapeBase.CoordOrigin property

الإحداثيات في الزاوية العلوية اليسرى للكتلة التي تحتوي على هذا الشكل.

```csharp
public Point CoordOrigin { get; set; }
```

### ملاحظات

القيمة الافتراضية هي (0,0).

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

يوضح كيفية إنشاء شكل مجموعة وتعبئته.

```csharp
Document doc = new Document();

// إنشاء شكل مجموعة. يمكن أن يعرض شكل المجموعة مجموعة من عقد الشكل التابعة.
// في Microsoft Word، سيؤدي النقر داخل حدود شكل المجموعة أو على أحد الأشكال الفرعية لشكل المجموعة إلى حدوث ذلك
// حدد جميع الأشكال الفرعية الأخرى ضمن هذه المجموعة واسمح لنا بقياس جميع الأشكال ونقلها مرة واحدة.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// قم بإنشاء شكل مجموعة بحجم 400pt x 400pt ووضعه عند أصل إحداثيات الشكل العائم للمستند.
group.Bounds = new RectangleF(0, 0, 400, 400);

// اضبط حجم مستوى الإحداثيات الداخلي للمجموعة على 500 × 500 نقطة. 
// سيكون للزاوية العلوية اليسرى من المجموعة إحداثيات x وy بقيمة (0، 0)،
// وسيكون للركن الأيمن السفلي إحداثيات x و y (500، 500).
group.CoordSize = new Size(500, 500);

// اضبط إحداثيات الزاوية العلوية اليسرى للمجموعة على (-250، -250). 
// سيكون لمركز المجموعة الآن قيمة إحداثية x وy قدرها (0، 0)،
// وسيكون الركن الأيمن السفلي عند (250، 250).
group.CoordOrigin = new Point(-250, -250);

// قم بإنشاء مستطيل يعرض حدود شكل المجموعة هذا وأضفه إلى المجموعة.
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
});

// بمجرد أن يصبح الشكل جزءًا من شكل مجموعة، يمكننا الوصول إليه كعقدة فرعية ثم تعديله.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// أنشئ نجمة حمراء صغيرة وأدخلها في المجموعة.
// قم بمحاذاة الشكل مع الأصل الإحداثي للمجموعة، والذي قمنا بنقله إلى المركز.
group.AppendChild(new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
});

// أدخل مستطيلاً، ثم أدخل مستطيلًا أصغر قليلاً في نفس المكان الذي يحتوي على صورة. 
// الأشكال الأحدث التي نضيفها إلى المجموعة تتداخل مع الأشكال القديمة. سوف يتداخل المستطيل الأزرق الفاتح جزئيًا مع النجمة الحمراء،
// وبعد ذلك سوف يتداخل الشكل مع الصورة مع المستطيل الأزرق الفاتح، ويستخدمه كإطار.
// لا يمكننا استخدام خصائص "ZOrder" للأشكال لمعالجة ترتيبها داخل شكل المجموعة. 
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

// أدخل مربع نص في شكل المجموعة. قم بتعيين الخاصية "يسار" بحيث تكون الحافة اليمنى لمربع النص
// يمس الحد الأيمن لشكل المجموعة. قم بتعيين الخاصية "Top" بحيث يكون مربع النص بالخارج
// حدود شكل المجموعة، بحيث يكون حجمها العلوي مصطفًا على طول الهامش السفلي لشكل المجموعة.
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


