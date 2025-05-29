---
title: ShapeBase.RelativeHorizontalPosition
linktitle: RelativeHorizontalPosition
articleTitle: RelativeHorizontalPosition
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase RelativeHorizontalPosition لإتقان تحديد المواقع الأفقية للأشكال. حسّن تصميمك بدقة وتحكم!
type: docs
weight: 450
url: /ar/net/aspose.words.drawing/shapebase/relativehorizontalposition/
---
## ShapeBase.RelativeHorizontalPosition property

يحدد بالنسبة إلى ما يتم وضع الشكل أفقيًا.

```csharp
public RelativeHorizontalPosition RelativeHorizontalPosition { get; set; }
```

## ملاحظات

القيمة الافتراضية هيColumn.

له تأثير فقط على الأشكال العائمة في المستوى العلوي.

## أمثلة

يوضح كيفية إدراج صورة عائمة في وسط الصفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج صورة عائمة ستظهر خلف النص المتداخل وقم بمحاذاتها مع مركز الصفحة.
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
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
