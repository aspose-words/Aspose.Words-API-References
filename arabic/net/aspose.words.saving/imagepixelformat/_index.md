---
title: ImagePixelFormat Enum
linktitle: ImagePixelFormat
articleTitle: ImagePixelFormat
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.ImagePixelFormat تعداد. يحدد تنسيق البكسل للصور التي تم إنشاؤها لصفحات المستند في C#.
type: docs
weight: 5220
url: /ar/net/aspose.words.saving/imagepixelformat/
---
## ImagePixelFormat enumeration

يحدد تنسيق البكسل للصور التي تم إنشاؤها لصفحات المستند.

```csharp
public enum ImagePixelFormat
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Format16BppRgb555 | `0` | 16 بت لكل بكسل، RGB. |
| Format16BppRgb565 | `1` | 16 بت لكل بكسل، RGB. |
| Format16BppArgb1555 | `2` | 16 بت لكل بكسل، ARGB. |
| Format24BppRgb | `3` | 24 بت لكل بكسل، RGB. |
| Format32BppRgb | `4` | 32 بت لكل بكسل، RGB. |
| Format32BppArgb | `5` | 32 بت لكل بكسل، ARGB. |
| Format32BppPArgb | `6` | 32 بت لكل بكسل، ARGB، ألفا المضاعف مسبقًا. |
| Format48BppRgb | `7` | 48 بت لكل بكسل، RGB. |
| Format64BppArgb | `8` | 64 بت لكل بكسل، ARGB. |
| Format64BppPArgb | `9` | 64 بت لكل بكسل، ARGB، ألفا المضاعف مسبقًا. |
| Format1bppIndexed | `10` | 1 بت لكل بكسل، مفهرسة. |

## أمثلة

يوضح كيفية تحديد معدل بت لكل بكسل لعرض مستند على صورة.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // عندما نحفظ المستند كصورة، يمكننا تمرير كائن SaveOptions إليه
            // حدد تنسيق البكسل للصورة التي ستنشئها عملية الحفظ.
            // ستؤثر معدلات البت المختلفة لكل بكسل على جودة الصورة التي تم إنشاؤها وحجمها.
            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
            imageSaveOptions.PixelFormat = imagePixelFormat;

            // يمكننا استنساخ مثيلات ImageSaveOptions.
            Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

            doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);

#if NET48 || JAVA
            switch (imagePixelFormat)
            {
                case ImagePixelFormat.Format1bppIndexed:
                    Assert.That(10000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format16BppRgb555:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format24BppRgb:
                    Assert.That(125000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format32BppRgb:
                    Assert.That(150000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format48BppRgb:
                    Assert.That(200000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
            }
#elif NET5_0_OR_GREATER
            switch (imagePixelFormat)
            {
                case ImagePixelFormat.Format1bppIndexed:
                    Assert.That(10000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format24BppRgb:
                    Assert.That(70000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format16BppRgb555:
                case ImagePixelFormat.Format32BppRgb:
                case ImagePixelFormat.Format48BppRgb:
                    Assert.That(125000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
            }
#endif
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
