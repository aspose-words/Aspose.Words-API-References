---
title: ShapeBase.BehindText
linktitle: BehindText
articleTitle: BehindText
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase BehindText للتحكم في طبقات الشكل في تصميماتك، مما يعزز رؤية النص ودقة التخطيط بسهولة.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing/shapebase/behindtext/
---
## ShapeBase.BehindText property

يحدد ما إذا كان الشكل أسفل النص أم فوقه.

```csharp
public bool BehindText { get; set; }
```

## ملاحظات

له تأثير فقط على الأشكال ذات المستوى الأعلى.

القيمة الافتراضية هي`خطأ شنيع`.

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

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
