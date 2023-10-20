---
title: ShapeBase.ZOrder
linktitle: ZOrder
articleTitle: ZOrder
second_title: Aspose.Words لـ .NET
description: ShapeBase ZOrder ملكية. تحديد ترتيب عرض الأشكال المتداخلة في C#.
type: docs
weight: 610
url: /ar/net/aspose.words.drawing/shapebase/zorder/
---
## ShapeBase.ZOrder property

تحديد ترتيب عرض الأشكال المتداخلة.

```csharp
public int ZOrder { get; set; }
```

## ملاحظات

له تأثير فقط على أشكال المستوى الأعلى.

القيمة الافتراضية هي 0.

يمثل الرقم أسبقية التراص. سيتم عرض الشكل ذو الرقم الأعلى كما لو كان متداخلاً (في "أمام" الشكل ذي الرقم الأقل.

ترتيب الأشكال المتداخلة مستقل عن الأشكال الموجودة في الرأس وفي النص الرئيسي للمستند.

يتم تحديد ترتيب عرض الأشكال الفرعية في شكل مجموعة حسب ترتيبها داخل شكل المجموعة.

## أمثلة

يوضح كيفية التعامل مع ترتيب الأشكال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل ثلاثة مستطيلات ملونة مختلفة تتداخل جزئيًا مع بعضها البعض.
// عندما نقوم بإدراج شكل يتداخل مع شكل آخر، فإن Aspose.Words يضع الشكل الأحدث فوق الشكل القديم.
// سوف يتداخل المستطيل الأخضر الفاتح مع المستطيل الأزرق الفاتح ويحجبه جزئيًا،
// وسيحجب المستطيل الأزرق الفاتح المستطيل البرتقالي.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);
shape.FillColor = Color.Orange;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 150,
    RelativeVerticalPosition.TopMargin, 150, 200, 200, WrapType.None);
shape.FillColor = Color.LightBlue;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 200, 200, WrapType.None);
shape.FillColor = Color.LightGreen;

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

// تحدد الخاصية "ZOrder" للشكل أولوية التراص بين الأشكال المتداخلة الأخرى.
// إذا كان هناك شكلان متداخلان لهما قيم "ZOrder" مختلفة،
// سيقوم Microsoft Word بوضع الشكل ذي القيمة الأعلى على الشكل ذي القيمة الأقل. 
// قم بتعيين قيم "ZOrder" للأشكال لدينا لوضع المستطيل البرتقالي الأول فوق المستطيل الأزرق الفاتح الثاني
// والمستطيل الأزرق الفاتح الثاني فوق المستطيل الأخضر الفاتح الثالث.
// سيؤدي هذا إلى عكس ترتيب التراص الأصلي.
shapes[0].ZOrder = 3;
shapes[1].ZOrder = 2;
shapes[2].ZOrder = 1;

doc.Save(ArtifactsDir + "Shape.ZOrder.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
