---
title: Class ThumbnailGeneratingOptions
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Rendering.ThumbnailGeneratingOptions فصل. يمكن استخدامها لتحديد خيارات إضافية عند إنشاء صورة مصغرة لمستند.
type: docs
weight: 4340
url: /ar/net/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class

يمكن استخدامها لتحديد خيارات إضافية عند إنشاء صورة مصغرة لمستند.

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
| [GenerateFromFirstPage](../../aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/) { get; set; } | يحدد ما إذا كان سيتم إنشاء مصغر من الصفحة الأولى من المستند أو الصورة الأولى. |
| [ThumbnailSize](../../aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/) { get; set; } | حجم الصورة المصغرة التي تم إنشاؤها بالبكسل . الافتراضي هو 600x900. |

### ملاحظات

يمكن للمستخدم استدعاء الطريقة[`UpdateThumbnail`](../../aspose.words/document/updatethumbnail/) لتوليد [`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) لمستند .

### أمثلة

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

// 2 - استخدم أول صورة موجودة في المستند:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Rendering](../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../)


