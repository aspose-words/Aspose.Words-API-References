---
title: "SaveOutputParameters"
linktitle: "SaveOutputParameters"
second_title: "Aspose.Words Java için"
description: "Bu nesne, bir belge kaydedildikten sonra çağırana döndürülür ve Java'daki kaydetme işlemi sırasında oluşturulan veya hesaplanan ek bilgileri içerir."
type: docs
weight: 597
url: /tr/java/com.aspose.words/saveoutputparameters/
---

**Inheritance:**
java.lang.Object
```
public class SaveOutputParameters
```

Bu nesne, bir belge kaydedildikten sonra çağırana döndürülür ve kaydetme işlemi sırasında oluşturulan veya hesaplanan ek bilgileri içerir. Çağıran bu nesneyi kullanabilir veya görmezden gelebilir.

Daha fazla bilgi edinmek için [ Save a Document ][Save a Document] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir belgenin kaydetme işleminin çıktı parametrelerine nasıl erişileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // After we save a document, we can access the Internet Media Type (MIME type) of the newly created output document.
 SaveOutputParameters parameters = doc.save(getArtifactsDir() + "Document.SaveOutputParameters.doc");

 Assert.assertEquals("application/msword", parameters.getContentType());

 // This property changes depending on the save format.
 parameters = doc.save(getArtifactsDir() + "Document.SaveOutputParameters.pdf");

 Assert.assertEquals("application/pdf", parameters.getContentType());
 
```


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getContentType()](#getContentType) | Kaydedilen belgenin türünü tanımlayan Content-Type dizesini (Internet Media Type) döndürür. |
### getContentType() {#getContentType}
```
public String getContentType()
```


Kaydedilen belgenin türünü tanımlayan Content-Type dizesini (Internet Media Type) döndürür.

 **Examples:** 

Bir belgenin kaydetme işleminin çıktı parametrelerine nasıl erişileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // After we save a document, we can access the Internet Media Type (MIME type) of the newly created output document.
 SaveOutputParameters parameters = doc.save(getArtifactsDir() + "Document.SaveOutputParameters.doc");

 Assert.assertEquals("application/msword", parameters.getContentType());

 // This property changes depending on the save format.
 parameters = doc.save(getArtifactsDir() + "Document.SaveOutputParameters.pdf");

 Assert.assertEquals("application/pdf", parameters.getContentType());
 
```

**Returns:**
java.lang.String - Kaydedilen belgenin türünü tanımlayan Content-Type dizesi (Internet Media Type).
