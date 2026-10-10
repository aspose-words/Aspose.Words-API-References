---
title: "WriteProtection"
linktitle: "WriteProtection"
second_title: "Aspose.Words Java için"
description: "Java'da bir belge için yazma koruması ayarlarını belirtir."
type: docs
weight: 738
url: /tr/java/com.aspose.words/writeprotection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class WriteProtection implements Cloneable
```

Bir belge için yazma koruması ayarlarını belirtir.

Daha fazla bilgi için, [ Protect or Encrypt a Document ][Protect or Encrypt a Document] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Yazma koruması, yazarın belgenin yalnızca okunur olarak açılmasını önerip önermediğini ve/veya belgeyi değiştirmek için bir şifre gerekip gerekmediğini belirtir.

Yazma koruması, belge korumasından farklıdır. Yazma koruması, Microsoft Word'de Farklı Kaydet iletişim kutusunun seçeneklerinde belirtilir.

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Belge koruma ayarlarına [Document.getWriteProtection()](../../com.aspose.words/document/\#getWriteProtection) özelliği aracılığıyla erişirsiniz.

 **Examples:** 

Bir belgeyi şifre ile nasıl koruyacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```


[Protect or Encrypt a Document]: https://docs.aspose.com/words/java/protect-or-encrypt-a-document/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getReadOnlyRecommended()](#getReadOnlyRecommended) | Belge yazarının belgenin yalnızca okunur olarak açılmasını önerip önermediğini belirtir. |
| [isWriteProtected()](#isWriteProtected) | Yazma koruma şifresi ayarlandığında  true  döndürür. |
| [setPassword(String password)](#setPassword-java.lang.String) | Belge için yazma koruma şifresini ayarlar. |
| [setReadOnlyRecommended(boolean value)](#setReadOnlyRecommended-boolean) | Belge yazarının belgenin yalnızca okunur olarak açılmasını önerip önermediğini belirtir. |
| [validatePassword(String password)](#validatePassword-java.lang.String) | Belirtilen şifre, belgenin korunduğu yazma koruma şifresiyle aynıysa  true  döndürür. |
### getReadOnlyRecommended() {#getReadOnlyRecommended}
```
public boolean getReadOnlyRecommended()
```


Belge yazarının belgenin yalnızca okunur olarak açılmasını önerip önermediğini belirtir.

 **Examples:** 

Bir belgeyi şifre ile nasıl koruyacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### isWriteProtected() {#isWriteProtected}
```
public boolean isWriteProtected()
```


Yazma koruma şifresi ayarlandığında  true  döndürür.

 **Examples:** 

Bir belgeyi şifre ile nasıl koruyacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Returns:**
boolean -  true  bir yazma koruma şifresi ayarlandığında.
### setPassword(String password) {#setPassword-java.lang.String}
```
public void setPassword(String password)
```


Belge için yazma koruma şifresini ayarlar.

 **Remarks:** 

Bir şifre ayarlanırsa, Microsoft Word kullanıcıdan şifreyi girmesini veya belgeyi yalnızca okunur olarak açmasını isteyecektir.

 **Examples:** 

Bir belgeyi şifre ile nasıl koruyacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| şifre | java.lang.String | Ayarlanacak şifre.  null  olamaz, ancak boş bir dize olabilir. |

### setReadOnlyRecommended(boolean value) {#setReadOnlyRecommended-boolean}
```
public void setReadOnlyRecommended(boolean value)
```


Belge yazarının belgenin yalnızca okunur olarak açılmasını önerip önermediğini belirtir.

 **Examples:** 

Bir belgeyi şifre ile nasıl koruyacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### validatePassword(String password) {#validatePassword-java.lang.String}
```
public boolean validatePassword(String password)
```


Belirtilen şifre, belgenin korunduğu yazma koruma şifresiyle aynıysa  true  döndürür. Belge şifreyle yazma korumalı değilse  false  döndürür.

 **Examples:** 

Bir belgeyi şifre ile nasıl koruyacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| şifre | java.lang.String |  |

**Returns:**
boolean
