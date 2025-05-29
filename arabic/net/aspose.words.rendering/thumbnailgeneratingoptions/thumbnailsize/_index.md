---
title: ThumbnailGeneratingOptions.ThumbnailSize
linktitle: ThumbnailSize
articleTitle: ThumbnailSize
second_title: Aspose.Words لـ .NET
description: اكتشف خيارات الصور المصغرة القابلة للتخصيص مع خاصية ThumbnailSize. أنشئ صورًا مصغرة مثالية بحجم بكسل، مع ضبطها افتراضيًا على 600×900 لعرض مثالي!
type: docs
weight: 30
url: /ar/net/aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/
---
## ThumbnailGeneratingOptions.ThumbnailSize property

حجم الصورة المصغرة المُولَّدة بالبكسل. الافتراضي هو 600x900.

```csharp
public Size ThumbnailSize { get; set; }
```

## أمثلة

يوضح كيفية تحديث الصورة المصغرة للمستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// هناك طريقتان لتعيين صورة مصغرة عند حفظ مستند بتنسيق .epub.
// 1 - استخدم الصفحة الأولى من المستند:
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

* class [ThumbnailGeneratingOptions](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)
