---
title: ShapeBase.VerticalAlignment
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. يحدد كيفية وضع الشكل عموديًا.
type: docs
weight: 560
url: /ar/net/aspose.words.drawing/shapebase/verticalalignment/
---
## ShapeBase.VerticalAlignment property

يحدد كيفية وضع الشكل عموديًا.

```csharp
public VerticalAlignment VerticalAlignment { get; set; }
```

### ملاحظات

القيمة الافتراضية هيNone.

له تأثير فقط على الأشكال العائمة ذات المستوى الأعلى.

### أمثلة

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

* enum [VerticalAlignment](../../verticalalignment/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


