---
title: "PdfEncryptionDetails"
linktitle: "PdfEncryptionDetails"
second_title: "Aspose.Words Java için"
description: "Java'da bir PDF belgesi için şifreleme ve erişim izinleriyle ilgili ayrıntıları içerir."
type: docs
weight: 534
url: /tr/java/com.aspose.words/pdfencryptiondetails/
---

**Inheritance:**
java.lang.Object
```
public class PdfEncryptionDetails
```

Bir PDF belgesinin şifrelenmesi ve erişim izinleriyle ilgili ayrıntıları içerir.

Daha fazla bilgi için, [ Protect or Encrypt a Document ][Protect or Encrypt a Document] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Kaydedilmiş bir PDF belgesinde izinlerin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```


[Protect or Encrypt a Document]: https://docs.aspose.com/words/java/protect-or-encrypt-a-document/
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [PdfEncryptionDetails(String userPassword, String ownerPassword)](#PdfEncryptionDetails-java.lang.String-java.lang.String) | Bu sınıfın bir örneğini başlatır. |
| [PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions)](#PdfEncryptionDetails-java.lang.String-java.lang.String-int) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getOwnerPassword()](#getOwnerPassword) | Şifrelenmiş PDF belgesi için sahibi şifresini belirtir. |
| [getPermissions()](#getPermissions) | Şifrelenmiş bir PDF belgesinde bir kullanıcıya izin verilen işlemleri belirtir. |
| [getUserPassword()](#getUserPassword) | Şifrelenmiş PDF belgesini açmak için gereken kullanıcı şifresini belirtir. |
| [setOwnerPassword(String value)](#setOwnerPassword-java.lang.String) | Şifrelenmiş PDF belgesi için sahibi şifresini belirtir. |
| [setPermissions(int value)](#setPermissions-int) | Şifrelenmiş bir PDF belgesinde bir kullanıcıya izin verilen işlemleri belirtir. |
| [setUserPassword(String value)](#setUserPassword-java.lang.String) | Şifrelenmiş PDF belgesini açmak için gereken kullanıcı şifresini belirtir. |
### PdfEncryptionDetails(String userPassword, String ownerPassword) {#PdfEncryptionDetails-java.lang.String-java.lang.String}
```
public PdfEncryptionDetails(String userPassword, String ownerPassword)
```


Bu sınıfın bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| userPassword | java.lang.String |  |
| ownerPassword | java.lang.String |  |

### PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions) {#PdfEncryptionDetails-java.lang.String-java.lang.String-int}
```
public PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| userPassword | java.lang.String |  |
| ownerPassword | java.lang.String |  |
| permissions | int |  |

### getOwnerPassword() {#getOwnerPassword}
```
public String getOwnerPassword()
```


Şifrelenmiş PDF belgesi için sahibi şifresini belirtir.

 **Remarks:** 

Sahibi şifresi, kullanıcının [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int) içinde belirtilen herhangi bir erişim kısıtlaması olmadan şifrelenmiş bir PDF belgesini açmasına izin verir.

Sahibi şifresi, kullanıcı şifresiyle aynı olamaz.

 **Examples:** 

Kaydedilmiş bir PDF belgesinde izinlerin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getPermissions() {#getPermissions}
```
public int getPermissions()
```


Şifrelenmiş bir PDF belgesinde bir kullanıcıya izin verilen işlemleri belirtir. Varsayılan değer [PdfPermissions.DISALLOW\_ALL](../../com.aspose.words/pdfpermissions/\#DISALLOW-ALL) dir.

 **Examples:** 

Kaydedilmiş bir PDF belgesinde izinlerin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Returns:**
int - İlgili  int  değeri. Döndürülen değer, [PdfPermissions](../../com.aspose.words/pdfpermissions/) sabitlerinin bit düzeyinde birleşimidir.
### getUserPassword() {#getUserPassword}
```
public String getUserPassword()
```


Şifrelenmiş PDF belgesini açmak için gereken kullanıcı şifresini belirtir.

 **Remarks:** 

Kullanıcı şifresi, şifrelenmiş bir PDF belgesini görüntülemek için açarken gerekecektir. [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int) içinde belirtilen izinler, okuyucu yazılımı tarafından uygulanacaktır.

Kullanıcı şifresi  null  veya boş bir dize olabilir; bu durumda PDF belgesi açılırken kullanıcıdan şifre istenmez. Kullanıcı şifresi, sahibi şifresiyle aynı olamaz.

 **Examples:** 

Kaydedilmiş bir PDF belgesinde izinlerin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### setOwnerPassword(String value) {#setOwnerPassword-java.lang.String}
```
public void setOwnerPassword(String value)
```


Şifrelenmiş PDF belgesi için sahibi şifresini belirtir.

 **Remarks:** 

Sahibi şifresi, kullanıcının [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int) içinde belirtilen herhangi bir erişim kısıtlaması olmadan şifrelenmiş bir PDF belgesini açmasına izin verir.

Sahibi şifresi, kullanıcı şifresiyle aynı olamaz.

 **Examples:** 

Kaydedilmiş bir PDF belgesinde izinlerin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setPermissions(int value) {#setPermissions-int}
```
public void setPermissions(int value)
```


Şifrelenmiş bir PDF belgesinde bir kullanıcıya izin verilen işlemleri belirtir. Varsayılan değer [PdfPermissions.DISALLOW\_ALL](../../com.aspose.words/pdfpermissions/\#DISALLOW-ALL) dir.

 **Examples:** 

Kaydedilmiş bir PDF belgesinde izinlerin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [PdfPermissions](../../com.aspose.words/pdfpermissions/) sabitlerinin bit düzeyinde birleşimi olmalıdır. |

### setUserPassword(String value) {#setUserPassword-java.lang.String}
```
public void setUserPassword(String value)
```


Şifrelenmiş PDF belgesini açmak için gereken kullanıcı şifresini belirtir.

 **Remarks:** 

Kullanıcı şifresi, şifrelenmiş bir PDF belgesini görüntülemek için açarken gerekecektir. [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int) içinde belirtilen izinler, okuyucu yazılımı tarafından uygulanacaktır.

Kullanıcı şifresi  null  veya boş bir dize olabilir; bu durumda PDF belgesi açılırken kullanıcıdan şifre istenmez. Kullanıcı şifresi, sahibi şifresiyle aynı olamaz.

 **Examples:** 

Kaydedilmiş bir PDF belgesinde izinlerin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

