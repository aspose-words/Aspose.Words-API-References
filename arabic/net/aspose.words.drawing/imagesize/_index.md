---
title: ImageSize Class
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.ImageSize فصل. يحتوي على معلومات حول حجم الصورة ودقتها في C#.
type: docs
weight: 1070
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
| [ImageSize](imagesize/#constructor)(*int, int*) | تهيئة العرض والارتفاع للقيم المحددة بالبكسل. تهيئة الدقة إلى 96 نقطة في البوصة. |
| [ImageSize](imagesize/#constructor_1)(*int, int, double, double*) | تهيئة العرض والارتفاع والدقة للقيم المحددة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [HeightPixels](../../aspose.words.drawing/imagesize/heightpixels/) { get; } | الحصول على ارتفاع الصورة بالبكسل. |
| [HeightPoints](../../aspose.words.drawing/imagesize/heightpoints/) { get; } | الحصول على ارتفاع الصورة بالنقاط. النقطة الواحدة هي 1/72 بوصة. |
| [HorizontalResolution](../../aspose.words.drawing/imagesize/horizontalresolution/) { get; } | الحصول على الدقة الأفقية بـ DPI. |
| [VerticalResolution](../../aspose.words.drawing/imagesize/verticalresolution/) { get; } | الحصول على الدقة الرأسية بـ DPI. |
| [WidthPixels](../../aspose.words.drawing/imagesize/widthpixels/) { get; } | الحصول على عرض الصورة بالبكسل. |
| [WidthPoints](../../aspose.words.drawing/imagesize/widthpoints/) { get; } | الحصول على عرض الصورة بالنقاط. النقطة الواحدة هي 1/72 بوصة. |

## أمثلة

يوضح كيفية تغيير حجم الشكل باستخدام الصورة.

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

            // عندما نقوم بإدراج صورة باستخدام طريقة "InsertImage"، يقوم المنشئ بقياس الشكل الذي يعرض الصورة بحيث،
            // عندما نعرض المستند باستخدام تكبير/تصغير بنسبة 100% في برنامج Microsoft Word، يعرض الشكل الصورة بحجمها الفعلي.
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

            // ستؤدي الصورة مقاس 400 × 400 إلى إنشاء كائن ImageData بحجم صورة يبلغ 300 × 300 نقطة.
            ImageSize imageSize = shape.ImageData.ImageSize;

            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // إذا كانت أبعاد الشكل تطابق أبعاد بيانات الصورة،
            // فإن الشكل يعرض الصورة بحجمها الأصلي.
            Assert.AreEqual(300.0d, shape.Width);
            Assert.AreEqual(300.0d, shape.Height);

             // تقليل الحجم الكلي للشكل بنسبة 50%.
            shape.Width *= 0.5;

             // تنطبق عوامل القياس على كل من العرض والارتفاع في نفس الوقت للحفاظ على تناسب الشكل.
            Assert.AreEqual(150.0d, shape.Width);
            Assert.AreEqual(150.0d, shape.Height);

            // عندما نقوم بتغيير حجم الشكل، يظل حجم بيانات الصورة كما هو.
            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // يمكننا الرجوع إلى أبعاد بيانات الصورة لتطبيق القياس بناءً على حجم الصورة.
            shape.Width = imageSize.WidthPoints * 1.1;

            Assert.AreEqual(330.0d, shape.Width);
            Assert.AreEqual(330.0d, shape.Height);

            doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### أنظر أيضا

* property [ImageSize](../imagedata/imagesize/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
