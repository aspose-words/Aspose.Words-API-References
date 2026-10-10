---
title: "ThumbnailGeneratingOptions"
linktitle: "ThumbnailGeneratingOptions"
second_title: "Aspose.Words Java için"
description: "Java'da bir belge için küçük resim oluştururken ek seçenekleri belirtmek için kullanılabilir."
type: docs
weight: 687
url: /tr/java/com.aspose.words/thumbnailgeneratingoptions/
---

**Inheritance:**
java.lang.Object
```
public class ThumbnailGeneratingOptions
```

Bir belge için küçük resim oluştururken ek seçenekler belirtmek için kullanılabilir.

 **Remarks:** 

Kullanıcı, bir belge için [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties/\#getThumbnail) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties/\#setThumbnail-byte) oluşturmak için [Document.updateThumbnail(com.aspose.words.ThumbnailGeneratingOptions)](../../com.aspose.words/document/\#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions) metodunu çağırabilir.

 **Examples:** 

Bir belgenin küçük resmini güncellemeyi gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getGenerateFromFirstPage()](#getGenerateFromFirstPage) | Küçük resmin belgenin ilk sayfasından mı yoksa ilk görselinden mi oluşturulacağını belirtir. |
| [getThumbnailSize()](#getThumbnailSize) | Oluşturulan küçük resmin boyutu piksel cinsinden. |
| [setGenerateFromFirstPage(boolean value)](#setGenerateFromFirstPage-boolean) | Küçük resmin belgenin ilk sayfasından mı yoksa ilk görselinden mi oluşturulacağını belirtir. |
| [setThumbnailSize(Dimension value)](#setThumbnailSize-java.awt.Dimension) | Oluşturulan küçük resmin boyutu piksel cinsinden. |
### getGenerateFromFirstPage() {#getGenerateFromFirstPage}
```
public boolean getGenerateFromFirstPage()
```


Küçük resmin belgenin ilk sayfasından mı yoksa ilk görselinden mi oluşturulacağını belirtir.

 **Remarks:** 

Varsayılan değer true'dir, bu da küçük resmin belgenin ilk sayfasından oluşturulacağı anlamına gelir. Değer false ise ve belgede resim yoksa, küçük resim yine belgenin ilk sayfasından oluşturulur.

 **Examples:** 

Bir belgenin küçük resmini güncellemeyi gösterir.

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
boolean - İlgili  boolean  değeri.
### getThumbnailSize() {#getThumbnailSize}
```
public Dimension getThumbnailSize()
```


Oluşturulan küçük resmin boyutu piksel cinsindendir. Varsayılan değer 600x900'dür.

 **Examples:** 

Bir belgenin küçük resmini güncellemeyi gösterir.

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
java.awt.Dimension - İlgili java.awt.Dimension değeri.
### setGenerateFromFirstPage(boolean value) {#setGenerateFromFirstPage-boolean}
```
public void setGenerateFromFirstPage(boolean value)
```


Küçük resmin belgenin ilk sayfasından mı yoksa ilk görselinden mi oluşturulacağını belirtir.

 **Remarks:** 

Varsayılan değer true'dir, bu da küçük resmin belgenin ilk sayfasından oluşturulacağı anlamına gelir. Değer false ise ve belgede resim yoksa, küçük resim yine belgenin ilk sayfasından oluşturulur.

 **Examples:** 

Bir belgenin küçük resmini güncellemeyi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setThumbnailSize(Dimension value) {#setThumbnailSize-java.awt.Dimension}
```
public void setThumbnailSize(Dimension value)
```


Oluşturulan küçük resmin boyutu piksel cinsindendir. Varsayılan değer 600x900'dür.

 **Examples:** 

Bir belgenin küçük resmini güncellemeyi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Dimension | İlgili java.awt.Dimension değeri. |

