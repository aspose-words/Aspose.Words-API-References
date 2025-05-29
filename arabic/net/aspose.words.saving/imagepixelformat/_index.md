---
title: ImagePixelFormat Enum
linktitle: ImagePixelFormat
articleTitle: ImagePixelFormat
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Saving.ImagePixelFormat للحصول على تنسيقات بكسل مثالية في صور صفحات المستندات. حسّن صور مستنداتك بسهولة!
type: docs
weight: 5970
url: /ar/net/aspose.words.saving/imagepixelformat/
---
## ImagePixelFormat enumeration

يحدد تنسيق البكسل للصور المولدة لصفحات المستند.

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
| Format32BppPArgb | `6` | 32 بت لكل بكسل، ARGB، ألفا مضاعف مسبقًا. |
| Format48BppRgb | `7` | 48 بت لكل بكسل، RGB. |
| Format64BppArgb | `8` | 64 بت لكل بكسل، ARGB. |
| Format64BppPArgb | `9` | 64 بت لكل بكسل، ARGB، ألفا مضاعف مسبقًا. |
| Format1bppIndexed | `10` | 1 بت لكل بكسل، مفهرس. |

## أمثلة

يوضح كيفية تحديد معدل البت لكل بكسل الذي سيتم به تحويل المستند إلى صورة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// عندما نحفظ المستند كصورة، يمكننا تمرير كائن SaveOptions إلى
// حدد تنسيق البكسل للصورة التي سيتم إنشاءها من خلال عملية الحفظ.
// ستؤثر معدلات البت المختلفة لكل بكسل على جودة وحجم ملف الصورة المولدة.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

//يمكننا استنساخ مثيلات ImageSaveOptions.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
