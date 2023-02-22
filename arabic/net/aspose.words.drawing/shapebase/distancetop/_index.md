---
title: ShapeBase.DistanceTop
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. إرجاع أو تحديد المسافة بالنقاط بين نص المستند والحافة العلوية للشكل.
type: docs
weight: 160
url: /ar/net/aspose.words.drawing/shapebase/distancetop/
---
## ShapeBase.DistanceTop property

إرجاع أو تحديد المسافة (بالنقاط) بين نص المستند والحافة العلوية للشكل.

```csharp
public double DistanceTop { get; set; }
```

### ملاحظات

القيمة الافتراضية هي 0.

له تأثير فقط لأشكال المستوى الأعلى.

### أمثلة

يوضح كيفية تعيين مسافة الالتفاف للنص الذي يحيط بالشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل مستطيلًا ، واجعل النص يلتف بإحكام حول حدوده.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 150, 150);
shape.WrapType = WrapType.Tight;

// اضبط الحد الأدنى للمسافة بين الشكل والنص المحيط على 40 نقطة من جميع الجوانب.
shape.DistanceTop = 40;
shape.DistanceBottom = 40;
shape.DistanceLeft = 40;
shape.DistanceRight = 40;

// حرك الشكل بالقرب من مركز الصفحة ، ثم قم بتدوير الشكل 60 درجة في اتجاه عقارب الساعة.
shape.Top = 75;
shape.Left = 150; 
shape.Rotation = 60;

// أضف نصًا سيلتف حول الشكل.
builder.Font.Size = 24;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "Shape.Coordinates.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


