---
title: ShapeBase.HorizontalAlignment
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. يحدد كيفية وضع الشكل أفقيًا.
type: docs
weight: 210
url: /ar/net/aspose.words.drawing/shapebase/horizontalalignment/
---
## ShapeBase.HorizontalAlignment property

يحدد كيفية وضع الشكل أفقيًا.

```csharp
public HorizontalAlignment HorizontalAlignment { get; set; }
```

### ملاحظات

النظام الأساسيNone.

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

* enum [HorizontalAlignment](../../horizontalalignment/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


