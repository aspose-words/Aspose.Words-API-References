---
title: ShapeBase.HorizontalAlignment
linktitle: HorizontalAlignment
articleTitle: HorizontalAlignment
second_title: Aspose.Words لـ .NET
description: ShapeBase HorizontalAlignment ملكية. يحدد كيفية وضع الشكل أفقيًا في C#.
type: docs
weight: 220
url: /ar/net/aspose.words.drawing/shapebase/horizontalalignment/
---
## ShapeBase.HorizontalAlignment property

يحدد كيفية وضع الشكل أفقيًا.

```csharp
public HorizontalAlignment HorizontalAlignment { get; set; }
```

## ملاحظات

القيمة الافتراضية هيNone.

له تأثير فقط على الأشكال العائمة ذات المستوى الأعلى.

## أمثلة

يوضح كيفية إدراج صورة عائمة في وسط الصفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل صورة عائمة ستظهر خلف النص المتداخل وقم بمحاذاتها مع منتصف الصفحة.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### أنظر أيضا

* enum [HorizontalAlignment](../../horizontalalignment/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
