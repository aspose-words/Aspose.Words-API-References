---
title: ShapeBase.Bottom
linktitle: Bottom
articleTitle: Bottom
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase Bottom للوصول بسهولة إلى موضع الحافة السفلية للكتلة التي تحتوي على الشكل الخاص بك للتحكم الدقيق في التصميم.
type: docs
weight: 60
url: /ar/net/aspose.words.drawing/shapebase/bottom/
---
## ShapeBase.Bottom property

يحصل على موضع الحافة السفلية للكتلة التي تحتوي على الشكل.

```csharp
public double Bottom { get; }
```

## ملاحظات

بالنسبة للشكل ذي المستوى الأعلى، تكون القيمة بالنقاط وبالنسبة لمرساة الشكل.

بالنسبة للأشكال الموجودة في مجموعة، تكون القيمة في مساحة الإحداثيات ووحدات المجموعة الأصلية.

## أمثلة

يوضح كيفية إدراج صورة عائمة وتحديد موضعها وحجمها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// قم بتكوين خاصية "RelativeHorizontalPosition" الخاصة بالشكل لمعالجة قيمة خاصية "Left"
 // كمسافة أفقية للشكل، بالنقاط، من الجانب الأيسر للصفحة.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// قم بتعيين المسافة الأفقية للشكل من الجانب الأيسر للصفحة إلى 100.
shape.Left = 100;

// استخدم خاصية "RelativeVerticalPosition" بطريقة مماثلة لوضع الشكل على مسافة 80 نقطة أسفل الجزء العلوي من الصفحة.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// قم بتعيين ارتفاع الشكل، والذي سيقوم تلقائيًا بتغيير العرض للحفاظ على الأبعاد.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// تحتوي خصائص "الأسفل" و"اليمين" على الحواف السفلية واليمنى للصورة.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
