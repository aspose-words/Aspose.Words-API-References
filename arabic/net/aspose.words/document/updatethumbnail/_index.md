---
title: Document.UpdateThumbnail
linktitle: UpdateThumbnail
articleTitle: UpdateThumbnail
second_title: Aspose.Words لـ .NET
description: Document UpdateThumbnail طريقة. التحديثاتThumbnail للمستند حسب الخيارات المحددة في C#.
type: docs
weight: 780
url: /ar/net/aspose.words/document/updatethumbnail/
---
## UpdateThumbnail(*[ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)*) {#updatethumbnail_1}

التحديثات[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) للمستند حسب الخيارات المحددة.

```csharp
public void UpdateThumbnail(ThumbnailGeneratingOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| options | ThumbnailGeneratingOptions | خيارات توليد للاستخدام. |

## ملاحظات

ال[`ThumbnailGeneratingOptions`](../../../aspose.words.rendering/thumbnailgeneratingoptions/) يسمح لك بتحديد مصدر الصورة المصغرة والحجم والخيارات الأخرى. إذا فشلت محاولة إنشاء صورة مصغرة، فلا يغير واحدة.

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

* class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## UpdateThumbnail() {#updatethumbnail}

التحديثات[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) للمستند باستخدام الخيارات الافتراضية.

```csharp
public void UpdateThumbnail()
```

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

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
