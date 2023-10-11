---
title: ShapeBase.Left
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. الحصول على أو تعيين موضع الحافة اليسرى للكتلة التي تحتوي على الشكل.
type: docs
weight: 370
url: /ar/net/aspose.words.drawing/shapebase/left/
---
## ShapeBase.Left property

الحصول على أو تعيين موضع الحافة اليسرى للكتلة التي تحتوي على الشكل.

```csharp
public double Left { get; set; }
```

### ملاحظات

بالنسبة لشكل المستوى الأعلى، تكون القيمة بالنقاط وترتبط بنقطة ارتساء الشكل.

بالنسبة للأشكال الموجودة في مجموعة، تكون القيمة في المساحة الإحداثية ووحدات المجموعة الأصلية.

القيمة الافتراضية هي 0.

له تأثير فقط على الأشكال العائمة.

### أمثلة

يوضح كيفية إدراج صورة عائمة وتحديد موضعها وحجمها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// قم بتكوين خاصية "RelativeHorizontalPosition" الخاصة بالشكل للتعامل مع قيمة الخاصية "اليسرى"
 // كالمسافة الأفقية للشكل، بالنقاط، من الجانب الأيسر للصفحة.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// اضبط المسافة الأفقية للشكل من الجانب الأيسر للصفحة على 100.
shape.Left = 100;

// استخدم خاصية "RelativeVerticalPosition" بطريقة مشابهة لوضع الشكل بمقدار 80 نقطة أسفل أعلى الصفحة.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// قم بتعيين ارتفاع الشكل، والذي سيقوم تلقائيًا بقياس العرض للحفاظ على الأبعاد.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// تحتوي الخصائص "السفلية" و"الأيمن" على الحواف السفلية واليمنى للصورة.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


