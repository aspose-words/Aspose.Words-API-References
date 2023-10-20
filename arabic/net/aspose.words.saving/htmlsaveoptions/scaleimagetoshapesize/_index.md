---
title: HtmlSaveOptions.ScaleImageToShapeSize
linktitle: ScaleImageToShapeSize
articleTitle: ScaleImageToShapeSize
second_title: Aspose.Words لـ .NET
description: HtmlSaveOptions ScaleImageToShapeSize ملكية. يحدد ما إذا كان سيتم تغيير حجم الصور بواسطة Aspose.Words إلى حجم الشكل المحيط عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيحقيقي  في C#.
type: docs
weight: 450
url: /ar/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

يحدد ما إذا كان سيتم تغيير حجم الصور بواسطة Aspose.Words إلى حجم الشكل المحيط عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

## ملاحظات

الصورة في مستند Microsoft Word هي شكل. الشكل له حجم وimage له حجمه الخاص. لا ترتبط الأحجام بشكل مباشر. على سبيل المثال، يمكن أن تكون الصورة 1024x786 بكسل، ولكن الشكل الذي يعرض هذه الصورة يمكن أن يكون 400x300 نقطة.

لكي يتم عرض صورة في المتصفح، يجب تغيير حجمها إلى حجم الشكل. `ScaleImageToShapeSize` تتحكم الخاصية في المكان الذي يتم فيه تغيير حجم الصورة image : في Aspose.Words أثناء التصدير إلى HTML أو في المتصفح عند عرض المستند.

متى`ScaleImageToShapeSize` يكون`حقيقي` ، يتم تغيير حجم الصورة بواسطة Aspose.Words باستخدام تحجيم عالي الجودة أثناء التصدير إلى HTML. متى`ScaleImageToShapeSize` هو`خطأ شنيع`، يتم إخراج الصورة بحجمها الأصلي ويجب على المتصفح تغيير حجمها.

بشكل عام، تقوم المتصفحات بتحجيم الجودة بسرعة وبطريقة رديئة. ونتيجة لذلك، ستحصل عادةً على جودة عرض أفضل في المتصفح وحجم ملف أصغر عندما`ScaleImageToShapeSize` يكون`حقيقي` ، ولكن جودة طباعة أفضل وتحويل أسرع عندما`ScaleImageToShapeSize` يكون`خطأ شنيع`.

بالإضافة إلى الأشكال التي تحتوي على صور نقطية فردية، يؤثر هذا الخيار أيضًا على أشكال المجموعة التي تتكون من من الصور النقطية. لو`ScaleImageToShapeSize` يكون`خطأ شنيع` ويحتوي شكل المجموعة على صور نقطية ذات دقة جوهرية أعلى من القيمة المحددة في[`ImageResolution`](../imageresolution/)، Aspose.Words سوف يزيد من دقة العرض لهذه المجموعة. يتيح ذلك الحفاظ بشكل أفضل على جودة الصور المجمعة ذات الدقة العالية عند الحفظ في HTML.

## أمثلة

يوضح كيفية تعطيل تغيير حجم الصور إلى أبعاد الشكل الأصلي الخاصة بها عند الحفظ في .html.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // قم بإدراج شكل يحتوي على صورة، ثم اجعل هذا الشكل أصغر بكثير من الصورة.
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

            Shape imageShape = builder.InsertImage(image);
            imageShape.Width = 50;
            imageShape.Height = 50;

            // سيؤدي حفظ مستند يحتوي على أشكال وصور بتنسيق HTML إلى إنشاء ملف صورة في نظام الملفات المحلي
            // لكل شكل من هذا القبيل. سيستخدم مستند HTML الناتج <image> علامات للارتباط بهذه الصور وعرضها.
            // عندما نحفظ المستند إلى HTML، يمكننا تمرير كائن SaveOptions لتحديده
            // ما إذا كان سيتم تغيير حجم جميع الصور الموجودة داخل الأشكال إلى أحجام أشكالها.
            // سيؤدي تعيين علامة "ScaleImageToShapeSize" على "true" إلى تقليص كل صورة
            // إلى حجم الشكل الذي يحتوي عليه، بحيث لا تكون الصور المحفوظة أكبر مما يتطلبه المستند.
            // سيؤدي تعيين علامة "ScaleImageToShapeSize" إلى "خطأ" إلى الحفاظ على الأحجام الأصلية لهذه الصور،
            // والتي ستشغل مساحة أكبر مقابل الحفاظ على جودة الصورة.
            HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

            doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);

            FileInfo fileInfo = new FileInfo(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.001.png");

#if NET48 || JAVA
        if (scaleImageToShapeSize)
            Assert.That(3000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(20000, Is.LessThan(fileInfo.Length));
#elif NET5_0_OR_GREATER
        if (scaleImageToShapeSize)
            Assert.That(10000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(30000, Is.LessThan(fileInfo.Length));
#endif
```

### أنظر أيضا

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
