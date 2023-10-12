---
title: ShapeBase.Bounds
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. الحصول على أو تعيين موقع وحجم الكتلة التي تحتوي على الشكل.
type: docs
weight: 70
url: /ar/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

الحصول على أو تعيين موقع وحجم الكتلة التي تحتوي على الشكل.

```csharp
public RectangleF Bounds { get; set; }
```

### ملاحظات

يتجاهل قفل نسبة العرض إلى الارتفاع عند الإعداد.

بالنسبة لشكل المستوى الأعلى، تكون القيمة بالنقاط وترتبط بنقطة ارتساء الشكل.

بالنسبة للأشكال الموجودة في مجموعة، تكون القيمة في المساحة الإحداثية ووحدات المجموعة الأصلية.

### أمثلة

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


