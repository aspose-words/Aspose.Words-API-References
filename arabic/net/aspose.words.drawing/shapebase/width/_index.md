---
title: ShapeBase.Width
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. الحصول على أو تحديد عرض الكتلة التي تحتوي على الشكل.
type: docs
weight: 520
url: /ar/net/aspose.words.drawing/shapebase/width/
---
## ShapeBase.Width property

الحصول على أو تحديد عرض الكتلة التي تحتوي على الشكل.

```csharp
public double Width { get; set; }
```

### ملاحظات

بالنسبة لشكل المستوى الأعلى ، تكون القيمة بالنقاط.

بالنسبة للأشكال في مجموعة ، تكون القيمة في مساحة الإحداثيات ووحدات المجموعة الأصلية.

القيمة الافتراضية هي 0.

### أمثلة

يوضح كيفية إدراج صورة عائمة ، وتحديد موضعها وحجمها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// تكوين خاصية "RelativeHorizontalPosition" للشكل لمعالجة قيمة الخاصية "Left"
 // كمسافة أفقية للشكل ، بالنقاط ، من الجانب الأيسر للصفحة.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// اضبط المسافة الأفقية للشكل من الجانب الأيسر للصفحة على 100.
shape.Left = 100;

// استخدم خاصية "RelativeVerticalPosition" بطريقة مماثلة لوضع الشكل 80 نقطة أسفل أعلى الصفحة.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// قم بتعيين ارتفاع الشكل ، والذي سيقيس العرض تلقائيًا للحفاظ على الأبعاد.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// تحتوي خصائص "الجزء السفلي" و "الأيمن" على الحواف السفلية واليمنى للصورة.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

يوضح كيفية تغيير حجم الشكل بصورة.

```csharp
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Logo.jpg");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

            // عندما نقوم بإدخال صورة باستخدام طريقة "InsertImage" ، يقوم المنشئ بقياس الشكل الذي يعرض الصورة بحيث ،
            // عندما نعرض المستند باستخدام تكبير بنسبة 100٪ في Microsoft Word ، يعرض الشكل الصورة بحجمها الفعلي.
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

            // ستؤدي الصورة مقاس 400 × 400 إلى إنشاء كائن ImageData بحجم صورة 300 × 300 نقطة.
            ImageSize imageSize = shape.ImageData.ImageSize;

            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // إذا كانت أبعاد الشكل تتطابق مع أبعاد بيانات الصورة ،
            // ثم يعرض الشكل الصورة بحجمها الأصلي.
            Assert.AreEqual(300.0d, shape.Width);
            Assert.AreEqual(300.0d, shape.Height);

             // تصغير الحجم الكلي للشكل بنسبة 50٪.
            shape.Width *= 0.5;

             // تنطبق عوامل القياس على كل من العرض والارتفاع في نفس الوقت للحفاظ على تناسب الشكل.
            Assert.AreEqual(150.0d, shape.Width);
            Assert.AreEqual(150.0d, shape.Height);

            // عندما نغير حجم الشكل ، يظل حجم بيانات الصورة كما هو.
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
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


