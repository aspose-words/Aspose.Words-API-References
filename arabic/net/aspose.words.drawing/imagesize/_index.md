---
title: ImageSize Class
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.ImageSize، وهي مصدرك المفضل للحصول على معلومات تفصيلية حول حجم الصورة ودقتها لتحسين جودة المستند.
type: docs
weight: 1400
url: /ar/net/aspose.words.drawing/imagesize/
---
## ImageSize class

يحتوي على معلومات حول حجم الصورة ودقتها.

لمعرفة المزيد، قم بزيارة[العمل مع الصور](https://docs.aspose.com/words/net/working-with-images/) مقالة توثيقية.

```csharp
public class ImageSize
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [ImageSize](imagesize/#constructor)(*int, int*) | يُهيئ العرض والارتفاع إلى القيم المحددة بالبكسل. يُهيئ الدقة إلى 96 نقطة في البوصة. |
| [ImageSize](imagesize/#constructor_1)(*int, int, double, double*) | يقوم بتهيئة العرض والارتفاع والدقة للقيم المحددة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [HeightPixels](../../aspose.words.drawing/imagesize/heightpixels/) { get; } | يحصل على ارتفاع الصورة بالبكسل. |
| [HeightPoints](../../aspose.words.drawing/imagesize/heightpoints/) { get; } | يحصل على ارتفاع الصورة بالنقاط. النقطة الواحدة هي 1/72 بوصة. |
| [HorizontalResolution](../../aspose.words.drawing/imagesize/horizontalresolution/) { get; } | يحصل على الدقة الأفقية بوحدة DPI. |
| [VerticalResolution](../../aspose.words.drawing/imagesize/verticalresolution/) { get; } | يحصل على الدقة الرأسية بوحدة DPI. |
| [WidthPixels](../../aspose.words.drawing/imagesize/widthpixels/) { get; } | يحصل على عرض الصورة بالبكسل. |
| [WidthPoints](../../aspose.words.drawing/imagesize/widthpoints/) { get; } | يحصل على عرض الصورة بالنقاط. النقطة الواحدة هي 1/72 بوصة. |

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

* property [ImageSize](../imagedata/imagesize/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
