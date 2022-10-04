---
title: Bounds
second_title: Aspose.Words لمراجع .NET API
description: الحصول على أو تحديد موقع وحجم الكتلة التي تحتوي على الشكل.
type: docs
weight: 70
url: /ar/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

الحصول على أو تحديد موقع وحجم الكتلة التي تحتوي على الشكل.

```csharp
public RectangleF Bounds { get; set; }
```

### ملاحظات

يتجاهل قفل نسبة العرض إلى الارتفاع عند الإعداد.

بالنسبة لشكل المستوى الأعلى ، تكون القيمة بالنقاط وتتناسب مع نقطة ارتساء الشكل.

بالنسبة للأشكال في مجموعة ، تكون القيمة في مساحة الإحداثيات ووحدات المجموعة الأصلية.

### أمثلة

يوضح كيفية التحقق من الشكل الذي يحتوي على حدود الكتلة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// على الرغم من أن السطر نفسه يشغل مساحة صغيرة على صفحة المستند ،
// يحتل كتلة مستطيلة الشكل ، ويمكن تحديد حجمها باستخدام خصائص "الحدود".
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// قم بإنشاء شكل مجموعة ، ثم قم بتعيين حجم الكتلة التي تحتوي عليها باستخدام خاصية "الحدود".
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// قم بإنشاء مستطيل ، وتحقق من حجم الكتلة المحيطة به ، ثم قم بإضافته إلى شكل المجموعة.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// يوجد أصل مستوى إحداثيات المجموعة في الزاوية العلوية اليسرى من الكتلة التي تحتوي عليها ،
// وإحداثيات x و y لـ (1000 ، 1000) في الركن الأيمن السفلي.
// يبلغ حجم شكل مجموعتنا 250 × 250 نقطة ، لذا فإن كل 4 نقاط على مستوى إحداثي شكل المجموعة
// يترجم إلى 1 نقطة في المستوى الإحداثي لهيكل الوثيقة.
// كل شكل نقوم بإدراجه سيتقلص حجمه أيضًا بمعامل 4.
// سيعكس التغيير في خاصية "BoundsInPoints" الخاصة بالشكل هذا.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// أدخل شكلًا وضعه خارج حدود الكتلة التي تحتوي على شكل المجموعة.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// زاد أثر شكل المجموعة في جسم المستند ، لكن الكتلة المحتوية تظل كما هي.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
