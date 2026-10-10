---
title: "PlainTextDocument"
linktitle: "PlainTextDocument"
second_title: "Aspose.Words Java için"
description: "Java'da belgenin içeriğinin düz metin temsilini çıkarmaya izin verir."
type: docs
weight: 549
url: /tr/java/com.aspose.words/plaintextdocument/
---

**Inheritance:**
java.lang.Object
```
public class PlainTextDocument
```

Belgenin içeriğinin düz metin temsilini çıkarmaya izin verir.

Daha fazla bilgi için, [ Working with Text Document ][Working with Text Document] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir Microsoft Word belgesinin içeriğini düz metin olarak nasıl yükleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PlainTextDocument.Load.docx");

 PlainTextDocument plaintext = new PlainTextDocument(getArtifactsDir() + "PlainTextDocument.Load.docx");

 Assert.assertEquals("Hello world!", plaintext.getText().trim());
 
```


[Working with Text Document]: https://docs.aspose.com/words/java/working-with-text-document/
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [PlainTextDocument(String fileName)](#PlainTextDocument-java.lang.String) | Bir dosyadan düz metin belge oluşturur. |
| [PlainTextDocument(String fileName, LoadOptions loadOptions)](#PlainTextDocument-java.lang.String-com.aspose.words.LoadOptions) | Bir dosyadan düz metin belge oluşturur. |
| [PlainTextDocument(InputStream stream)](#PlainTextDocument-java.io.InputStream) | Bu sınıfın yeni bir örneğini başlatır. |
| [PlainTextDocument(InputStream stream, LoadOptions loadOptions)](#PlainTextDocument-java.io.InputStream-com.aspose.words.LoadOptions) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getBuiltInDocumentProperties()](#getBuiltInDocumentProperties) | Belgenin [getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getBuiltInDocumentProperties) özelliklerini alır. |
| [getCustomDocumentProperties()](#getCustomDocumentProperties) | Belgenin [getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getCustomDocumentProperties) özelliklerini alır. |
| [getText()](#getText) | Belgenin metinsel içeriğini bir dize olarak birleştirir. |
### PlainTextDocument(String fileName) {#PlainTextDocument-java.lang.String}
```
public PlainTextDocument(String fileName)
```


Bir dosyadan düz metin belge oluşturur. Dosya biçimini otomatik olarak algılar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Metni çıkarılacak dosyanın adı. |

### PlainTextDocument(String fileName, LoadOptions loadOptions) {#PlainTextDocument-java.lang.String-com.aspose.words.LoadOptions}
```
public PlainTextDocument(String fileName, LoadOptions loadOptions)
```


Bir dosyadan düz metin belge oluşturur. Şifreleme parolası gibi ek seçenekleri belirtmeye izin verir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Metni çıkarılacak dosyanın adı. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Bir belge yüklerken kullanılacak ek seçenekler. null olabilir. |

### PlainTextDocument(InputStream stream) {#PlainTextDocument-java.io.InputStream}
```
public PlainTextDocument(InputStream stream)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### PlainTextDocument(InputStream stream, LoadOptions loadOptions) {#PlainTextDocument-java.io.InputStream-com.aspose.words.LoadOptions}
```
public PlainTextDocument(InputStream stream, LoadOptions loadOptions)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) |  |

### getBuiltInDocumentProperties() {#getBuiltInDocumentProperties}
```
public BuiltInDocumentProperties getBuiltInDocumentProperties()
```


Belgenin [getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getBuiltInDocumentProperties) özelliklerini alır.

 **Examples:** 

Bir Microsoft Word belgesinin içeriğini düz metin olarak nasıl yükleyeceğinizi ve ardından orijinal belgenin yerleşik özelliklerine nasıl erişeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");

 doc.save(getArtifactsDir() + "PlainTextDocument.BuiltInProperties.docx");

 PlainTextDocument plaintext = new PlainTextDocument(getArtifactsDir() + "PlainTextDocument.BuiltInProperties.docx");

 Assert.assertEquals("Hello world!", plaintext.getText().trim());
 Assert.assertEquals("John Doe", plaintext.getBuiltInDocumentProperties().getAuthor());
 
```

**Returns:**
[BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties/) - [getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getBuiltInDocumentProperties) of the document.
### getCustomDocumentProperties() {#getCustomDocumentProperties}
```
public CustomDocumentProperties getCustomDocumentProperties()
```


Belgenin [getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getCustomDocumentProperties) özelliklerini alır.

 **Examples:** 

Microsoft Word belgesinin içeriğini düz metin olarak nasıl yükleyeceğinizi ve ardından orijinal belgenin özel özelliklerine nasıl erişileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 doc.getCustomDocumentProperties().add("Location of writing", "123 Main St, London, UK");

 doc.save(getArtifactsDir() + "PlainTextDocument.CustomDocumentProperties.docx");

 PlainTextDocument plaintext = new PlainTextDocument(getArtifactsDir() + "PlainTextDocument.CustomDocumentProperties.docx");

 Assert.assertEquals("Hello world!", plaintext.getText().trim());
 Assert.assertEquals("123 Main St, London, UK", plaintext.getCustomDocumentProperties().get("Location of writing").getValue());
 
```

**Returns:**
[CustomDocumentProperties](../../com.aspose.words/customdocumentproperties/) - [getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getCustomDocumentProperties) of the document.
### getText() {#getText}
```
public String getText()
```


Belgenin metinsel içeriğini bir dize olarak birleştirir.

 **Examples:** 

Bir Microsoft Word belgesinin içeriğini düz metin olarak nasıl yükleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PlainTextDocument.Load.docx");

 PlainTextDocument plaintext = new PlainTextDocument(getArtifactsDir() + "PlainTextDocument.Load.docx");

 Assert.assertEquals("Hello world!", plaintext.getText().trim());
 
```

**Returns:**
java.lang.String - Belgenin metinsel içeriğinin bir dize olarak birleştirilmiş hali.
