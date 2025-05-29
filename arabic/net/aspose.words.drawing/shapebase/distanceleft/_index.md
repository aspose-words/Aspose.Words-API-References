---
title: ShapeBase.DistanceLeft
linktitle: DistanceLeft
articleTitle: DistanceLeft
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase DistanceLeft لضبط المسافة بالنقاط بسهولة بين نص المستند والحافة اليسرى للأشكال للتحكم المحسّن في التخطيط.
type: docs
weight: 140
url: /ar/net/aspose.words.drawing/shapebase/distanceleft/
---
## ShapeBase.DistanceLeft property

يقوم بإرجاع أو تعيين المسافة (بالنقاط) بين نص المستند والحافة اليسرى للشكل.

```csharp
public double DistanceLeft { get; set; }
```

## ملاحظات

القيمة الافتراضية هي 1/8 بوصة.

له تأثير فقط على الأشكال ذات المستوى الأعلى.

## أمثلة

يوضح كيفية تعيين مسافة الالتفاف للنص المحيط بالشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل مستطيلاً، واجعل النص يلتف بإحكام حول حدوده.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 150, 150);
shape.WrapType = WrapType.Tight;

// قم بتعيين الحد الأدنى للمسافة بين الشكل والنص المحيط به إلى 40 نقطة من جميع الجوانب.
shape.DistanceTop = 40;
shape.DistanceBottom = 40;
shape.DistanceLeft = 40;
shape.DistanceRight = 40;

// حرك الشكل أقرب إلى مركز الصفحة، ثم قم بتدوير الشكل 60 درجة في اتجاه عقارب الساعة.
shape.Top = 75;
shape.Left = 150;
shape.Rotation = 60;

//أضف نصًا يلتف حول الشكل.
builder.Font.Size = 24;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "Shape.Coordinates.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
