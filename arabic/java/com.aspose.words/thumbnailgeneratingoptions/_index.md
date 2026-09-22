---
title: "ThumbnailGeneratingOptions"
linktitle: "ThumbnailGeneratingOptions"
second_title: "Aspose.Words لـ Java"
description: "يمكن استخدامه لتحديد خيارات إضافية عند إنشاء صورة مصغرة لمستند في Java."
type: docs
weight: 687
url: /ar/java/com.aspose.words/thumbnailgeneratingoptions/
---

**Inheritance:**
java.lang.Object
```
public class ThumbnailGeneratingOptions
```

يمكن استخدامه لتحديد خيارات إضافية عند إنشاء صورة مصغرة لمستند.

 **Remarks:** 

يمكن للمستخدم استدعاء الطريقة [Document.updateThumbnail(com.aspose.words.ThumbnailGeneratingOptions)](../../com.aspose.words/document/\#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions) لإنشاء [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties/\#getThumbnail) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties/\#setThumbnail-byte) للمستند.

 **Examples:** 

يعرض كيفية تحديث الصورة المصغرة للمستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getGenerateFromFirstPage()](#getGenerateFromFirstPage) | يحدد ما إذا كان سيتم إنشاء الصورة المصغرة من الصفحة الأولى للمستند أو من الصورة الأولى. |
| [getThumbnailSize()](#getThumbnailSize) | حجم الصورة المصغرة المُولَّدة بالبكسل. |
| [setGenerateFromFirstPage(boolean value)](#setGenerateFromFirstPage-boolean) | يحدد ما إذا كان سيتم إنشاء الصورة المصغرة من الصفحة الأولى للمستند أو من الصورة الأولى. |
| [setThumbnailSize(Dimension value)](#setThumbnailSize-java.awt.Dimension) | حجم الصورة المصغرة المُولَّدة بالبكسل. |
### getGenerateFromFirstPage() {#getGenerateFromFirstPage}
```
public boolean getGenerateFromFirstPage()
```


يحدد ما إذا كان سيتم إنشاء الصورة المصغرة من الصفحة الأولى للمستند أو من الصورة الأولى.

 **Remarks:** 

القيمة الافتراضية هي  true  ، مما يعني أنه سيتم إنشاء الصورة المصغرة من الصفحة الأولى للمستند. إذا كانت القيمة  false  ولا توجد صورة في المستند، سيتم إنشاء الصورة المصغرة من الصفحة الأولى للمستند.

 **Examples:** 

يعرض كيفية تحديث الصورة المصغرة للمستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getThumbnailSize() {#getThumbnailSize}
```
public Dimension getThumbnailSize()
```


حجم الصورة المصغرة المُولَّدة بالبكسل. القيمة الافتراضية هي 600x900.

 **Examples:** 

يعرض كيفية تحديث الصورة المصغرة للمستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```

**Returns:**
java.awt.Dimension - القيمة المقابلة لـ java.awt.Dimension.
### setGenerateFromFirstPage(boolean value) {#setGenerateFromFirstPage-boolean}
```
public void setGenerateFromFirstPage(boolean value)
```


يحدد ما إذا كان سيتم إنشاء الصورة المصغرة من الصفحة الأولى للمستند أو من الصورة الأولى.

 **Remarks:** 

القيمة الافتراضية هي  true  ، مما يعني أنه سيتم إنشاء الصورة المصغرة من الصفحة الأولى للمستند. إذا كانت القيمة  false  ولا توجد صورة في المستند، سيتم إنشاء الصورة المصغرة من الصفحة الأولى للمستند.

 **Examples:** 

يعرض كيفية تحديث الصورة المصغرة للمستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setThumbnailSize(Dimension value) {#setThumbnailSize-java.awt.Dimension}
```
public void setThumbnailSize(Dimension value)
```


حجم الصورة المصغرة المُولَّدة بالبكسل. القيمة الافتراضية هي 600x900.

 **Examples:** 

يعرض كيفية تحديث الصورة المصغرة للمستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Dimension | القيمة المقابلة لـ java.awt.Dimension. |

