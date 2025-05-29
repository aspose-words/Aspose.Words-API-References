---
title: ImageSize.HeightPoints
linktitle: HeightPoints
articleTitle: HeightPoints
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImageSize HeightPoints لاسترجاع ارتفاع الصورة بالنقاط بسهولة - النقطة الواحدة تساوي 1/72 بوصة. حسّن صورك بسهولة!
type: docs
weight: 30
url: /ar/net/aspose.words.drawing/imagesize/heightpoints/
---
## ImageSize.HeightPoints property

يحصل على ارتفاع الصورة بالنقاط. النقطة الواحدة هي 1/72 بوصة.

```csharp
public double HeightPoints { get; }
```

## أمثلة

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

* class [ImageSize](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
