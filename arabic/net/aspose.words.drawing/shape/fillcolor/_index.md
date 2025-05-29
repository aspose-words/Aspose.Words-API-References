---
title: Shape.FillColor
linktitle: FillColor
articleTitle: FillColor
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Shape FillColor لتخصيص تصميماتك بألوان فرشاة نابضة بالحياة تعمل على تحسين أشكالك وترتقي بمشاريعك.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing/shape/fillcolor/
---
## Shape.FillColor property

يحدد لون الفرشاة التي تملأ المسار المغلق للشكل.

```csharp
public Color FillColor { get; set; }
```

## ملاحظات

هذا اختصار لـ[`Color`](../../fill/color/) ملكية.

القيمة الافتراضية هي White .

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

* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
