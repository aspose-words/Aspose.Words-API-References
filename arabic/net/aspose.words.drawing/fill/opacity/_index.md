---
title: Fill.Opacity
linktitle: Opacity
articleTitle: Opacity
second_title: Aspose.Words لـ .NET
description: يمكنك التحكم في شفافية التصميم الخاص بك باستخدام خاصية Fill Opacity، وضبط الوضوح من شفاف تمامًا إلى معتم تمامًا للحصول على صور مذهلة.
type: docs
weight: 150
url: /ar/net/aspose.words.drawing/fill/opacity/
---
## Fill.Opacity property

يحصل على درجة تعتيم التعبئة المحددة أو يضبطها كقيمة بين 0.0 (واضح) و1.0 (غير شفاف).

```csharp
public double Opacity { get; set; }
```

## ملاحظات

هذه الخاصية هي عكس الخاصية[`Transparency`](../transparency/).

## أمثلة

يوضح كيفية ملء الشكل بلون ثابت.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// اكتب بعض النص، ثم قم بتغطيته بشكل عائم.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

//استخدم خاصية "StrokeColor" لتعيين لون الخطوط العريضة للشكل.
shape.StrokeColor = Color.CadetBlue;

//استخدم خاصية "FillColor" لتعيين لون المنطقة الداخلية للشكل.
shape.FillColor = Color.LightBlue;

// تحدد خاصية "الشفافية" مدى شفافية اللون على مقياس من 0 إلى 1،
// حيث 1 يكون معتمًا تمامًا، و0 يكون غير مرئي.
// يتم تعبئة الشكل بشكل افتراضي بشكل معتم بالكامل، وبالتالي لا يمكننا رؤية النص الموجود أعلى هذا الشكل.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// قم بضبط تعتيم لون تعبئة الشكل إلى قيمة أقل حتى نتمكن من رؤية النص الموجود أسفله.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### أنظر أيضا

* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
