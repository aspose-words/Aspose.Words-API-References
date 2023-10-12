---
title: ShapeBase.CanHaveImage
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. إرجاعحقيقي إذا كان نوع الشكل يسمح للشكل بأن يكون له صورة.
type: docs
weight: 100
url: /ar/net/aspose.words.drawing/shapebase/canhaveimage/
---
## ShapeBase.CanHaveImage property

إرجاع`حقيقي` إذا كان نوع الشكل يسمح للشكل بأن يكون له صورة.

```csharp
public bool CanHaveImage { get; }
```

### ملاحظات

على الرغم من أن Microsoft Word يحتوي على نوع شكل خاص للصور، إلا أنه يبدو أنه في مستندات Microsoft Word يمكن لأي شكل باستثناء شكل المجموعة أن يحتوي على صورة، وبالتالي ترجع هذه الخاصية`حقيقي` لجميع الأشكال ما عدا[`GroupShape`](../../groupshape/).

### أمثلة

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
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


