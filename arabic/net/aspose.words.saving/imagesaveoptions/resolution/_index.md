---
title: ImageSaveOptions.Resolution
second_title: Aspose.Words لمراجع .NET API
description: ImageSaveOptions ملكية. يضبط الدقة الأفقية والرأسية للصور التي تم إنشاؤها  بالنقاط في البوصة .
type: docs
weight: 120
url: /ar/net/aspose.words.saving/imagesaveoptions/resolution/
---
## ImageSaveOptions.Resolution property

يضبط الدقة الأفقية والرأسية للصور التي تم إنشاؤها ، بالنقاط في البوصة .

```csharp
public float Resolution { set; }
```

### ملاحظات

هذه الخاصية لها تأثير فقط عند الحفظ بتنسيقات صور نقطية.

### أمثلة

يوضح كيفية تحديد دقة أثناء تقديم مستند إلى PNG.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

            // قم بإنشاء كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "حفظ" المستند
            // لتعديل الطريقة التي تعرض بها هذه الطريقة المستند إلى صورة.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

            // اضبط خاصية "Resolution" على "72" لتقديم المستند بدقة 72 نقطة في البوصة.
            options.Resolution = 72;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

            Assert.That(120000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png").Length));

#if NET48 || JAVA
            Image image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png");

            Assert.AreEqual(612, image.Width);
            Assert.AreEqual(792, image.Height);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png")) 
            {
                Assert.AreEqual(612, image.Width);
                Assert.AreEqual(792, image.Height);
            }
#endif
            // اضبط خاصية "Resolution" على "300" لتقديم المستند بدقة 300 نقطة في البوصة.
            options.Resolution = 300;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);

            Assert.That(700000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png").Length));

#if NET48 || JAVA
            image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png");

            Assert.AreEqual(2550, image.Width);
            Assert.AreEqual(3300, image.Height);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png")) 
            {
                Assert.AreEqual(2550, image.Width);
                Assert.AreEqual(3300, image.Height);
            }
#endif
```

### أنظر أيضا

* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../imagesaveoptions/)
* المجسم [Aspose.Words](../../../)


