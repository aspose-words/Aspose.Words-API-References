---
title: ShapeBase.RelativeVerticalPosition
linktitle: RelativeVerticalPosition
articleTitle: RelativeVerticalPosition
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase RelativeVerticalPosition لتحسين المحاذاة الرأسية للأشكال، مما يضمن التحكم الدقيق في التخطيط في تصميماتك.
type: docs
weight: 470
url: /ar/net/aspose.words.drawing/shapebase/relativeverticalposition/
---
## ShapeBase.RelativeVerticalPosition property

يحدد بالنسبة إلى الوضع الرأسي للشكل.

```csharp
public RelativeVerticalPosition RelativeVerticalPosition { get; set; }
```

## ملاحظات

القيمة الافتراضية هيParagraph.

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

* enum [RelativeVerticalPosition](../../relativeverticalposition/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
