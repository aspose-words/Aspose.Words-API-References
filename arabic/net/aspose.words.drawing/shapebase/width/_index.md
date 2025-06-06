---
title: ShapeBase.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية عرض قاعدة الشكل. اضبط بسهولة عرض الكتلة التي تحتوي على الشكل لتحسين مرونة ودقة التصميم.
type: docs
weight: 610
url: /ar/net/aspose.words.drawing/shapebase/width/
---
## ShapeBase.Width property

يحصل على عرض الكتلة التي تحتوي على الشكل أو يعينه.

```csharp
public double Width { get; set; }
```

## ملاحظات

بالنسبة للشكل ذي المستوى الأعلى، تكون القيمة بالنقاط.

بالنسبة للأشكال الموجودة في مجموعة، تكون القيمة في مساحة الإحداثيات ووحدات المجموعة الأصلية.

القيمة الافتراضية هي 0.

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

يوضح كيفية تغيير حجم الشكل باستخدام الصورة.

```csharp
// عندما نقوم بإدراج صورة باستخدام طريقة "InsertImage"، يقوم المنشئ بقياس الشكل الذي يعرض الصورة بحيث،
// عندما نقوم بعرض المستند باستخدام تكبير 100% في Microsoft Word، يعرض الشكل الصورة بحجمها الفعلي.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// ستؤدي الصورة ذات الحجم 400x400 إلى إنشاء كائن ImageData بحجم صورة 300x300pt.
ImageSize imageSize = shape.ImageData.ImageSize;

Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// إذا كانت أبعاد الشكل تتطابق مع أبعاد بيانات الصورة،
// ثم يقوم الشكل بعرض الصورة بحجمها الأصلي.
Assert.AreEqual(300.0d, shape.Width);
Assert.AreEqual(300.0d, shape.Height);

 //تقليل الحجم الإجمالي للشكل بنسبة 50%.
shape.Width *= 0.5;

 // يتم تطبيق عوامل القياس على كل من العرض والارتفاع في نفس الوقت للحفاظ على نسب الشكل.
Assert.AreEqual(150.0d, shape.Width);
Assert.AreEqual(150.0d, shape.Height);

// عندما نقوم بتغيير حجم الشكل، يظل حجم بيانات الصورة كما هو.
Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// يمكننا الرجوع إلى أبعاد بيانات الصورة لتطبيق مقياس بناءً على حجم الصورة.
shape.Width = imageSize.WidthPoints * 1.1;

Assert.AreEqual(330.0d, shape.Width);
Assert.AreEqual(330.0d, shape.Height);

doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
