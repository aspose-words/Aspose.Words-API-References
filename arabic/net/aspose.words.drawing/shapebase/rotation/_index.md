---
title: ShapeBase.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase Rotation، وقم بتحديد وتخصيص زوايا الدوران لأشكالك بسهولة، مما يعزز دقة تصميمك وإبداعه.
type: docs
weight: 500
url: /ar/net/aspose.words.drawing/shapebase/rotation/
---
## ShapeBase.Rotation property

يحدد الزاوية (بالدرجات) التي يدور بها الشكل. القيمة الإيجابية تتوافق مع زاوية الدوران في اتجاه عقارب الساعة.

```csharp
public double Rotation { get; set; }
```

## ملاحظات

القيمة الافتراضية هي 0.

## أمثلة

يوضح كيفية إدراج صورة وتدويرها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إدراج شكل مع صورة.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// قم بتدوير الصورة 45 درجة في اتجاه عقارب الساعة.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
