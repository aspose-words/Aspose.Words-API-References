---
title: ShapeBase.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words لـ .NET
description: ShapeBase Rotation ملكية. تحدد الزاوية بالدرجات التي يتم تدوير الشكل بها. القيمة الموجبة تتوافق مع زاوية الدوران في اتجاه عقارب الساعة في C#.
type: docs
weight: 470
url: /ar/net/aspose.words.drawing/shapebase/rotation/
---
## ShapeBase.Rotation property

تحدد الزاوية (بالدرجات) التي يتم تدوير الشكل بها. القيمة الموجبة تتوافق مع زاوية الدوران في اتجاه عقارب الساعة.

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

// أدخل شكلاً مع صورة.
Shape shape = builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
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
