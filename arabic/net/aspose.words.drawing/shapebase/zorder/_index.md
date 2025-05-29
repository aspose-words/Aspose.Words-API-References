---
title: ShapeBase.ZOrder
linktitle: ZOrder
articleTitle: ZOrder
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية ShapeBase ZOrder على تعزيز تصميمك من خلال التحكم في ترتيب عرض الأشكال المتداخلة للحصول على تخطيط أكثر وضوحًا وتنظيمًا.
type: docs
weight: 650
url: /ar/net/aspose.words.drawing/shapebase/zorder/
---
## ShapeBase.ZOrder property

يحدد ترتيب عرض الأشكال المتداخلة.

```csharp
public int ZOrder { get; set; }
```

## ملاحظات

له تأثير فقط على الأشكال ذات المستوى الأعلى.

القيمة الافتراضية هي 0.

يُمثل الرقم أولوية التكديس. سيظهر الشكل ذو الرقم الأعلى x000d_ كما لو كان متداخلاً (أمام) مع الشكل ذي الرقم الأقل.

يعتبر ترتيب الأشكال المتداخلة مستقلاً بالنسبة للأشكال الموجودة في الرأس وفي النص الرئيسي للمستند.

يتم تحديد ترتيب عرض الأشكال الفرعية في شكل المجموعة من خلال order داخل شكل المجموعة.

## أمثلة

يوضح كيفية التحكم في ترتيب الأشكال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل ثلاثة مستطيلات بألوان مختلفة تتداخل جزئيًا مع بعضها البعض.
// عندما نقوم بإدراج شكل يتداخل مع شكل آخر، يقوم Aspose.Words بوضع الشكل الأحدث فوق الشكل القديم.
// سوف يتداخل المستطيل الأخضر الفاتح مع المستطيل الأزرق الفاتح ويخفيه جزئيًا،
// والمستطيل الأزرق الفاتح سوف يحجب المستطيل البرتقالي.
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

// تحدد خاصية "ZOrder" الخاصة بالشكل أولوية التكديس بين الأشكال المتداخلة الأخرى.
// إذا كان لشكلين متداخلين قيم "ZOrder" مختلفة،
 // سيقوم Microsoft Word بوضع الشكل الذي يحمل القيمة الأعلى فوق الشكل الذي يحمل القيمة الأقل.
// اضبط قيم "ZOrder" لأشكالنا لوضع المستطيل البرتقالي الأول فوق المستطيل الأزرق الفاتح الثاني
// والمستطيل الأزرق الفاتح الثاني فوق المستطيل الأخضر الفاتح الثالث.
// سيؤدي هذا إلى عكس ترتيب التكديس الأصلي.
shapes[0].ZOrder = 3;
shapes[1].ZOrder = 2;
shapes[2].ZOrder = 1;

doc.Save(ArtifactsDir + "Shape.ZOrder.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
