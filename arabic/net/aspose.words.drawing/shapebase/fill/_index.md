---
title: ShapeBase.Fill
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية تعبئة ShapeBase لتحسين تصميماتك باستخدام تنسيق تعبئة قابل للتخصيص للأشكال. حسّن صورك بكل سهولة!
type: docs
weight: 170
url: /ar/net/aspose.words.drawing/shapebase/fill/
---
## ShapeBase.Fill property

يحصل على تنسيق التعبئة للشكل.

```csharp
public Fill Fill { get; }
```

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

* class [Fill](../../fill/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
