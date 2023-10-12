---
title: ShapeBase.DistanceBottom
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. إرجاع أو تعيين المسافة بالنقاط بين نص المستند والحافة السفلية للشكل.
type: docs
weight: 130
url: /ar/net/aspose.words.drawing/shapebase/distancebottom/
---
## ShapeBase.DistanceBottom property

إرجاع أو تعيين المسافة (بالنقاط) بين نص المستند والحافة السفلية للشكل.

```csharp
public double DistanceBottom { get; set; }
```

### ملاحظات

القيمة الافتراضية هي 0.

له تأثير فقط على أشكال المستوى الأعلى.

### أمثلة

يوضح كيفية تعيين مسافة الالتفاف للنص الذي يحيط بالشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل مستطيلاً واجعل النص يلتف بإحكام حول حدوده.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 150, 150);
shape.WrapType = WrapType.Tight;

// اضبط الحد الأدنى للمسافة بين الشكل والنص المحيط على 40 نقطة من جميع الجوانب.
shape.DistanceTop = 40;
shape.DistanceBottom = 40;
shape.DistanceLeft = 40;
shape.DistanceRight = 40;

// حرك الشكل بالقرب من منتصف الصفحة، ثم قم بتدوير الشكل 60 درجة في اتجاه عقارب الساعة.
shape.Top = 75;
shape.Left = 150; 
shape.Rotation = 60;

// أضف نصًا يلتف حول الشكل.
builder.Font.Size = 24;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "Shape.Coordinates.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


