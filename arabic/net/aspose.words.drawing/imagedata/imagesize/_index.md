---
title: ImageData.ImageSize
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImageData ImageSize للوصول بسهولة إلى التفاصيل الأساسية حول أبعاد الصورة ودقتها لتحسين جودة الصورة.
type: docs
weight: 130
url: /ar/net/aspose.words.drawing/imagedata/imagesize/
---
## ImageData.ImageSize property

يحصل على معلومات حول حجم الصورة ودقتها.

```csharp
public ImageSize ImageSize { get; }
```

## ملاحظات

إذا تم ربط الصورة فقط ولم يتم تخزينها في المستند، فسيتم إرجاع الحجم إلى صفر.

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

* class [ImageSize](../../imagesize/)
* class [ImageData](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
