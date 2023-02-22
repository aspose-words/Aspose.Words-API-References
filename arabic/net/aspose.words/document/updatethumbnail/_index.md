---
title: Document.UpdateThumbnail
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. التحديثاتThumbnail من المستند وفقًا للخيارات المحددة.
type: docs
weight: 760
url: /ar/net/aspose.words/document/updatethumbnail/
---
## UpdateThumbnail(ThumbnailGeneratingOptions) {#updatethumbnail_1}

التحديثات[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) من المستند وفقًا للخيارات المحددة.

```csharp
public void UpdateThumbnail(ThumbnailGeneratingOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| options | ThumbnailGeneratingOptions | خيارات توليد للاستخدام. |

### ملاحظات

ملف[`ThumbnailGeneratingOptions`](../../../aspose.words.rendering/thumbnailgeneratingoptions/) يسمح لك بتحديد مصدر الصورة المصغرة والحجم وخيارات أخرى.

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

* class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

---

## UpdateThumbnail() {#updatethumbnail}

التحديثات[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) من المستند باستخدام الخيارات الافتراضية.

```csharp
public void UpdateThumbnail()
```

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

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


