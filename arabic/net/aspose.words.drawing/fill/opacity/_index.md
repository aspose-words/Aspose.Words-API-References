---
title: Fill.Opacity
second_title: Aspose.Words لمراجع .NET API
description: Fill ملكية. الحصول على درجة تعتيم التعبئة المحددة أو تعيينها كقيمة بين 0.0 واضح و 1.0 معتم .
type: docs
weight: 90
url: /ar/net/aspose.words.drawing/fill/opacity/
---
## Fill.Opacity property

الحصول على درجة تعتيم التعبئة المحددة أو تعيينها كقيمة بين 0.0 (واضح) و 1.0 (معتم) .

```csharp
public double Opacity { get; set; }
```

### ملاحظات

هذه الخاصية هي عكس الممتلكات[`Transparency`](../transparency/).

### أمثلة

يوضح كيفية تعبئة شكل بلون خالص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// اكتب بعض النص ، ثم قم بتغطيته بشكل عائم.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// استخدم خاصية "StrokeColor" لتعيين لون المخطط التفصيلي للشكل.
shape.StrokeColor = Color.CadetBlue;

// استخدم خاصية "FillColor" لتعيين لون المنطقة الداخلية للشكل.
shape.FillColor = Color.LightBlue;

// تحدد خاصية "العتامة" مدى شفافية اللون على مقياس من 0-1 ،
// مع كون 1 معتمًا تمامًا ، والصفر غير مرئي.
// يكون ملء الشكل افتراضيًا معتمًا تمامًا ، لذلك لا يمكننا رؤية النص الموجود في أعلى هذا الشكل.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// اضبط عتامة لون تعبئة الشكل على قيمة أقل حتى نتمكن من رؤية النص تحتها.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### أنظر أيضا

* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../fill/)
* المجسم [Aspose.Words](../../../)


