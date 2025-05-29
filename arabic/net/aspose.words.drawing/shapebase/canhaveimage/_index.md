---
title: ShapeBase.CanHaveImage
linktitle: CanHaveImage
articleTitle: CanHaveImage
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase CanHaveImage—تعرف على كيفية تحديد ما إذا كان نوع الشكل الخاص بك يدعم الصور لتحسين الجاذبية البصرية!
type: docs
weight: 100
url: /ar/net/aspose.words.drawing/shapebase/canhaveimage/
---
## ShapeBase.CanHaveImage property

إرجاع`حقيقي` إذا كان نوع الشكل يسمح للشكل بالحصول على صورة.

```csharp
public bool CanHaveImage { get; }
```

## ملاحظات

على الرغم من أن Microsoft Word لديه نوع شكل خاص للصور، يبدو أنه في مستندات Microsoft Word يمكن لأي شكل باستثناء شكل المجموعة أن يحتوي على صورة، وبالتالي فإن هذه الخاصية ترجع`حقيقي` لجميع الأشكال باستثناء[`GroupShape`](../../groupshape/).

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
