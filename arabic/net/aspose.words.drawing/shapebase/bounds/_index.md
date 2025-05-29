---
title: ShapeBase.Bounds
linktitle: Bounds
articleTitle: Bounds
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase Bounds لإدارة موقع وحجم الشكل بسهولة، مما يعزز دقة التصميم وكفاءته.
type: docs
weight: 70
url: /ar/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

يحصل على أو يعين موقع وحجم الكتلة التي تحتوي على الشكل.

```csharp
public RectangleF Bounds { get; set; }
```

## ملاحظات

يتجاهل قفل نسبة العرض إلى الارتفاع عند الضبط.

بالنسبة للشكل ذي المستوى الأعلى، تكون القيمة بالنقاط وبالنسبة لمرساة الشكل.

بالنسبة للأشكال الموجودة في مجموعة، تكون القيمة في مساحة الإحداثيات ووحدات المجموعة الأصلية.

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
