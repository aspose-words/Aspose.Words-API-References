---
title: DocumentBuilder.InsertGroupShape
linktitle: InsertGroupShape
articleTitle: InsertGroupShape
second_title: Aspose.Words لـ .NET
description: قم بتجميع الأشكال بسهولة باستخدام طريقة InsertGroupShape في DocumentBuilder. أنشئ تصميمات منظمة بإدراج عقد GroupShape جديدة بسلاسة.
type: docs
weight: 360
url: /ar/net/aspose.words/documentbuilder/insertgroupshape/
---
## InsertGroupShape(*params ShapeBase[]*) {#insertgroupshape}

تجميع الأشكال التي تم تمريرها كمعلمة في عقدة GroupShape جديدة يتم إدراجها في الموضع الحالي.

```csharp
public GroupShape InsertGroupShape(params ShapeBase[] shapes)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| shapes | ShapeBase[] | قائمة الأشكال المراد تجميعها. |

## ملاحظات

سيتم حساب موضع وأبعاد GroupShape الجديد تلقائيًا.

لا يمكن تجميع أشكال VML وDML معًا.

## أمثلة

يوضح كيفية دمج شكل المجموعة مع الشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// قم بدمج الأشكال في عقدة GroupShape والتي يتم إدراجها في الموضع المحدد.
GroupShape groupShape1 = builder.InsertGroupShape(shape1, shape2);

// دمج عقد الشكل وعقدة المجموعة.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(groupShape1, shape3);

doc.Save(ArtifactsDir + "Shape.CombineGroupShape.docx");
```

يوضح كيفية إدراج شكل مجموعة DML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// أبعاد عقدة GroupShape الجديدة.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// إدراج عقدة GroupShape للحجم المحدد والتي يتم إدراجها في الموضع المحدد.
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// أدخل عقدة GroupShape التي سيتم حساب موضعها وأبعادها تلقائيًا.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### أنظر أيضا

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertGroupShape(*double, double, double, double, params ShapeBase[]*) {#insertgroupshape_1}

تجميع الأشكال التي تم تمريرها كمعلمة في عقدة GroupShape جديدة بالحجم المحدد والتي يتم إدراجها في الموضع المحدد.

```csharp
public GroupShape InsertGroupShape(double left, double top, double width, double height, 
    params ShapeBase[] shapes)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| left | Double | المسافة بالنقاط من الأصل إلى الجانب الأيسر لشكل المجموعة. |
| top | Double | المسافة بالنقاط من الأصل إلى الجانب العلوي لشكل المجموعة. |
| width | Double | عرض شكل المجموعة بالنقاط. لا يُسمح بالقيمة السالبة. |
| height | Double | ارتفاع شكل المجموعة بالنقاط. لا يُسمح بالقيمة السالبة. |
| shapes | ShapeBase[] | قائمة الأشكال المراد تجميعها. |

## ملاحظات

لا يمكن تجميع أشكال VML وDML معًا.

## أمثلة

يوضح كيفية إدراج شكل مجموعة DML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// أبعاد عقدة GroupShape الجديدة.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// إدراج عقدة GroupShape للحجم المحدد والتي يتم إدراجها في الموضع المحدد.
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// أدخل عقدة GroupShape التي سيتم حساب موضعها وأبعادها تلقائيًا.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### أنظر أيضا

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
