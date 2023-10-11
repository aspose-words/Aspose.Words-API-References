---
title: ImageSaveOptions.ImageColorMode
second_title: Aspose.Words لمراجع .NET API
description: ImageSaveOptions ملكية. الحصول على أو تعيين وضع الألوان للصور التي تم إنشاؤها.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/imagesaveoptions/imagecolormode/
---
## ImageSaveOptions.ImageColorMode property

الحصول على أو تعيين وضع الألوان للصور التي تم إنشاؤها.

```csharp
public ImageColorMode ImageColorMode { get; set; }
```

### ملاحظات

تؤثر هذه الخاصية فقط عند الحفظ في تنسيقات الصور النقطية.

القيمة الافتراضية هيNone.

### أمثلة

يوضح كيفية ضبط وضع الألوان عند عرض المستندات.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // عندما نحفظ المستند كصورة، يمكننا تمرير كائن SaveOptions إليه
            // حدد وضع الألوان للصورة التي ستنشئها عملية الحفظ.
            // إذا قمنا بتعيين خاصية "ImageColorMode" على "ImageColorMode.BlackAndWhite"،
            // ستطبق عملية الحفظ تقليل اللون الرمادي أثناء عرض المستند.
            // إذا قمنا بتعيين خاصية "ImageColorMode" على "ImageColorMode.Grayscale"،
            // ستعمل عملية الحفظ على تحويل المستند إلى صورة أحادية اللون.
            // إذا قمنا بتعيين خاصية "ImageColorMode" على "لا شيء"، فستطبق عملية الحفظ الطريقة الافتراضية
            // والحفاظ على جميع ألوان المستند في الصورة الناتجة.
            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
            imageSaveOptions.ImageColorMode = imageColorMode;

            doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);

#if NET48 || JAVA
            switch (imageColorMode)
            {
                case ImageColorMode.None:
                    Assert.That(150000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.Grayscale:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.BlackAndWhite:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
            }
#elif NET5_0_OR_GREATER
            switch (imageColorMode)
            {
                case ImageColorMode.None:
                    Assert.That(120000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.Grayscale:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.BlackAndWhite:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
            }
#endif
```

### أنظر أيضا

* enum [ImageColorMode](../../imagecolormode/)
* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../imagesaveoptions/)
* المجسم [Aspose.Words](../../../)


