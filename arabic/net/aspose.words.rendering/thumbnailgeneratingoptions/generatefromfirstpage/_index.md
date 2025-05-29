---
title: ThumbnailGeneratingOptions.GenerateFromFirstPage
linktitle: GenerateFromFirstPage
articleTitle: GenerateFromFirstPage
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يقوم خيار GenerateFromFirstPage بإنشاء صور مصغرة من الصفحة الأولى أو الصورة الخاصة بالمستند، مما يعزز المحتوى المرئي الخاص بك بسهولة.
type: docs
weight: 20
url: /ar/net/aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/
---
## ThumbnailGeneratingOptions.GenerateFromFirstPage property

يحدد ما إذا كان سيتم إنشاء صورة مصغرة من الصفحة الأولى من المستند أو الصورة الأولى.

```csharp
public bool GenerateFromFirstPage { get; set; }
```

## ملاحظات

الافتراضي هو`حقيقي` ، مما يعني أنه سيتم إنشاء الصورة المصغرة من الصفحة الأولى من المستند. إذا كانت القيمة`خطأ شنيع` وإذا لم تكن هناك صورة في المستند، فسيتم إنشاء الصورة المصغرة من الصفحة الأولى من المستند.

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
