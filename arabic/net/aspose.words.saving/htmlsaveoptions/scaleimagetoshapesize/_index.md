---
title: HtmlSaveOptions.ScaleImageToShapeSize
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد ما إذا كان يتم قياس الصور بواسطة Aspose.Words لحجم الشكل المحيط عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيحقيقي .
type: docs
weight: 450
url: /ar/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

يحدد ما إذا كان يتم قياس الصور بواسطة Aspose.Words لحجم الشكل المحيط عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

### ملاحظات

الصورة في مستند Microsoft Word عبارة عن شكل. الشكل له حجم والصورة image لها حجمها الخاص. الأحجام غير مرتبطة بشكل مباشر. على سبيل المثال ، يمكن أن تكون الصورة 1024 × 786 بكسل ، لكن الشكل الذي يعرض هذه الصورة يمكن أن يكون 400 × 300 نقطة.

لعرض صورة في المستعرض ، يجب تغيير حجمها إلى حجم الشكل`ScaleImageToShapeSize` تتحكم الخاصية في مكان تغيير حجم image : في Aspose.Words أثناء التصدير إلى HTML أو في المتصفح عند عرض المستند.

متي`ScaleImageToShapeSize` هو`حقيقي` ، يتم قياس الصورة بواسطة Aspose.Words باستخدام تحجيم عالي الجودة أثناء التصدير إلى HTML. متي`ScaleImageToShapeSize` هو`خاطئة`، يتم إخراج الصورة بحجمها الأصلي ويجب على المتصفح تغيير حجمها.

بشكل عام ، تقوم المتصفحات بتحجيم جودة سريعة وضعيفة. نتيجة لذلك ، ستحصل عادةً على جودة عرض أفضل في المتصفح وحجم ملف أصغر عندما`ScaleImageToShapeSize` هو`حقيقي` ، لكن جودة طباعة أفضل وتحويل أسرع عندما`ScaleImageToShapeSize` هو`خاطئة`.

### أمثلة

يوضح كيفية تعطيل تحجيم الصور لأبعاد الشكل الأصلية عند الحفظ في .html.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // أدخل شكلًا يحتوي على صورة ، ثم اجعل هذا الشكل أصغر بكثير من الصورة.
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

            // سيؤدي حفظ مستند يحتوي على أشكال بها صور إلى HTML إلى إنشاء ملف صورة في نظام الملفات المحلي
            // لكل شكل من هذا القبيل. سيستخدم مستند HTML الناتج العلامة < image > العلامات لربط وعرض هذه الصور.
            // عندما نحفظ المستند إلى HTML ، يمكننا تمرير كائن SaveOptions لتحديده
            // ما إذا كان سيتم تغيير حجم جميع الصور الموجودة داخل الأشكال إلى أحجام أشكالها.
            // سيؤدي تعيين علامة "ScaleImageToShapeSize" إلى "true" إلى تقليص كل صورة
            // إلى حجم الشكل الذي يحتوي عليه ، بحيث لا تكون الصور المحفوظة أكبر مما يتطلبه المستند.
            // سيؤدي تعيين علامة "ScaleImageToShapeSize" على "خطأ" إلى الحفاظ على الأحجام الأصلية لهذه الصور ،
            // والتي سوف تشغل مساحة أكبر مقابل الحفاظ على جودة الصورة.
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
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


