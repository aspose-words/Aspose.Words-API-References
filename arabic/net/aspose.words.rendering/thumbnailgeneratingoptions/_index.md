---
title: ThumbnailGeneratingOptions Class
linktitle: ThumbnailGeneratingOptions
articleTitle: ThumbnailGeneratingOptions
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Rendering.ThumbnailGeneratingOptions فصل. يمكن استخدامه لتحديد خيارات إضافية عند إنشاء صورة مصغرة للمستند في C#.
type: docs
weight: 4600
url: /ar/net/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class

يمكن استخدامه لتحديد خيارات إضافية عند إنشاء صورة مصغرة للمستند.

```csharp
public class ThumbnailGeneratingOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [ThumbnailGeneratingOptions](thumbnailgeneratingoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [GenerateFromFirstPage](../../aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/) { get; set; } | يحدد ما إذا كان سيتم إنشاء صورة مصغرة من الصفحة الأولى للمستند أو الصورة الأولى. |
| [ThumbnailSize](../../aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/) { get; set; } | حجم الصورة المصغرة التي تم إنشاؤها بالبكسل. الافتراضي هو 600x900. |

## ملاحظات

يمكن للمستخدم الاتصال بالطريقة[`UpdateThumbnail`](../../aspose.words/document/updatethumbnail/) لتوليد [`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) للمستند.

## أمثلة

يوضح كيفية تحديث الصورة المصغرة للمستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// هناك طريقتان لتعيين صورة مصغرة عند حفظ مستند إلى .epub.
// 1 - استخدم الصفحة الأولى للمستند:
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 - استخدم الصورة الأولى الموجودة في المستند:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Rendering](../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../)
