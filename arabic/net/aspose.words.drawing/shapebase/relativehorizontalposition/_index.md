---
title: ShapeBase.RelativeHorizontalPosition
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. تحديد متعلق بالموضع الأفقي للشكل.
type: docs
weight: 400
url: /ar/net/aspose.words.drawing/shapebase/relativehorizontalposition/
---
## ShapeBase.RelativeHorizontalPosition property

تحديد متعلق بالموضع الأفقي للشكل.

```csharp
public RelativeHorizontalPosition RelativeHorizontalPosition { get; set; }
```

### ملاحظات

النظام الأساسيColumn.

له تأثير فقط للأشكال العائمة ذات المستوى الأعلى.

### أمثلة

يوضح كيفية إدراج صورة عائمة في وسط الصفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل صورة عائمة ستظهر خلف النص المتداخل وقم بمحاذاة مركز الصفحة.
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

* enum [RelativeHorizontalPosition](../../relativehorizontalposition/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


