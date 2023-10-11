---
title: Fill.Opacity
second_title: Aspose.Words لمراجع .NET API
description: Fill ملكية. الحصول على أو تعيين درجة عتامة التعبئة المحددة كقيمة تتراوح بين 0.0 واضح و1.0 معتم.
type: docs
weight: 150
url: /ar/net/aspose.words.drawing/fill/opacity/
---
## Fill.Opacity property

الحصول على أو تعيين درجة عتامة التعبئة المحددة كقيمة تتراوح بين 0.0 (واضح) و1.0 (معتم).

```csharp
public double Opacity { get; set; }
```

### ملاحظات

هذه الخاصية هي عكس الملكية[`Transparency`](../transparency/).

### أمثلة

يوضح كيفية تعبئة الشكل بلون خالص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// اكتب بعض النص، ثم قم بتغطيته بشكل عائم.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// استخدم خاصية "StrokeColor" لتعيين لون المخطط التفصيلي للشكل.
shape.StrokeColor = Color.CadetBlue;

// استخدم خاصية "FillColor" لتعيين لون المنطقة الداخلية من الشكل.
shape.FillColor = Color.LightBlue;

// تحدد خاصية "العتامة" مدى شفافية اللون على مقياس من 0 إلى 1،
// مع كون 1 معتمًا تمامًا، و0 غير مرئي.
// تكون تعبئة الشكل معتمة تمامًا بشكل افتراضي، لذا لا يمكننا رؤية النص الذي يوجد هذا الشكل فوقه.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// اضبط عتامة لون تعبئة الشكل على قيمة أقل حتى نتمكن من رؤية النص الموجود أسفله.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### أنظر أيضا

* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../fill/)
* المجسم [Aspose.Words](../../../)


