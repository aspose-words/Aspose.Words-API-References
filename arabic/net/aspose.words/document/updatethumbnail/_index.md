---
title: Document.UpdateThumbnail
linktitle: UpdateThumbnail
articleTitle: UpdateThumbnail
second_title: Aspose.Words لـ .NET
description: حدّث الصورة المصغرة لمستندك بسهولة باستخدام خياراتنا القابلة للتخصيص. حسّن صورك وحسّن عرض مستندك اليوم!
type: docs
weight: 840
url: /ar/net/aspose.words/document/updatethumbnail/
---
## UpdateThumbnail(*[ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)*) {#updatethumbnail_1}

تحديثات [`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) من المستند وفقًا للخيارات المحددة.

```csharp
public void UpdateThumbnail(ThumbnailGeneratingOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| options | ThumbnailGeneratingOptions | خيارات التوليد للاستخدام. |

## ملاحظات

ال[`ThumbnailGeneratingOptions`](../../../aspose.words.rendering/thumbnailgeneratingoptions/) يسمح لك بتحديد مصدر الصورة المصغرة والحجم والخيارات الأخرى. إذا فشلت محاولة إنشاء الصورة المصغرة، فلا يتم تغييرها.

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

* class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## UpdateThumbnail() {#updatethumbnail}

تحديثات [`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) من المستند باستخدام الخيارات الافتراضية.

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

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
