---
title: "DigitalSignature"
linktitle: "DigitalSignature"
second_title: "Aspose.Words для Java"
description: "Представляет цифровую подпись документа и результат её проверки в Java."
type: docs
weight: 150
url: /ru/java/com.aspose.words/digitalsignature/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignature
```

Представляет цифровую подпись документа и результат её проверки.

Чтобы узнать больше, посетите статью документации [ Work with Digital Signatures ][Work with Digital Signatures].

 **Examples:** 

Показывает, как проверять и отображать информацию о каждой подписи в документе.

```

 Document doc = new Document(getMyDir() + "Digitally signed.docx");

 for (DigitalSignature signature : doc.getDigitalSignatures()) {
     System.out.println("*** Signature Found ***");
     System.out.println("Is valid: " + signature.isValid());
     // This property is available in MS Word documents only
     System.out.println("Reason for signing: " + signature.getComments());
     System.out.println("Signature type: " + signature.getSignatureType());
     System.out.println("Time of signing: " + signature.getSignTime());
     System.out.println("Subject name: " + signature.getSubjectName());
     System.out.println("Issuer name: " + signature.getIssuerName());
     System.out.println();
 }
 
```


[Work with Digital Signatures]: https://docs.aspose.com/words/java/working-with-digital-signatures/
## Методы

| Метод | Описание |
| --- | --- |
| [getApplicationVersion()](#getApplicationVersion) | Получает версию приложения для цифровой подписи. |
| [getCertificateHolder()](#getCertificateHolder) | Возвращает объект держателя сертификата, содержащий сертификат, использованный для подписи документа. |
| [getColorDepth()](#getColorDepth) | Получает глубину цвета для цифровой подписи. |
| [getComments()](#getComments) | Получает комментарий о цели подписи. |
| [getHorizontalResolution()](#getHorizontalResolution) | Получает горизонтальное разрешение цифровой подписи. |
| [getIssuerName()](#getIssuerName) | Возвращает отличительное имя субъекта сертификата издателя. |
| [getOfficeVersion()](#getOfficeVersion) | Получает версию Office для цифровой подписи. |
| [getSignTime()](#getSignTime) | Получает время подписи документа. |
| [getSignatureType()](#getSignatureType) | Получает тип цифровой подписи. |
| [getSignatureValue()](#getSignatureValue) | Получает массив байтов, представляющих значение подписи. |
| [getSubjectName()](#getSubjectName) | Возвращает отличительное имя субъекта сертификата, который использовался для подписи документа. |
| [getVerticalResolution()](#getVerticalResolution) | Получает вертикальное разрешение цифровой подписи. |
| [getWindowsVersion()](#getWindowsVersion) | Получает версию Windows для цифровой подписи. |
| [isValid()](#isValid) | Возвращает  true  если эта цифровая подпись действительна и документ не был изменён. |
| [toString()](#toString) | Возвращает удобочитаемую строку, отображающую значение этого объекта. |
### getApplicationVersion() {#getApplicationVersion}
```
public String getApplicationVersion()
```


Получает версию приложения для цифровой подписи.

**Returns:**
java.lang.String — версия приложения для цифровой подписи.
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Возвращает объект держателя сертификата, содержащий сертификат, использованный для подписи документа.

 **Examples:** 

Показывает, как подписывать документы с помощью сертификатов X.509.

```

 // Verify that a document is not signed.
 Assert.assertFalse(FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx").hasDigitalSignature());

 // Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);

 SignOptions signOptions = new SignOptions();
 signOptions.setSignTime(new Date());

 // There are two ways of saving a signed copy of a document to the local file system:
 // 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "Document.DigitalSignature.docx",
         certificateHolder, signOptions);

 Assert.assertTrue(FileFormatUtil.detectFileFormat(getArtifactsDir() + "Document.DigitalSignature.docx").hasDigitalSignature());

 // 2 - Take a document from a stream, and save a signed copy to another stream.
 InputStream inDoc = new FileInputStream(getMyDir() + "Document.docx");
 try {
     OutputStream outDoc = new FileOutputStream(getArtifactsDir() + "Document.DigitalSignature.docx");
     try {
         DigitalSignatureUtil.sign(inDoc, outDoc, certificateHolder);
     } finally {
         if (outDoc != null) outDoc.close();
     }
 } finally {
     if (inDoc != null) inDoc.close();
 }

 Assert.assertTrue(FileFormatUtil.detectFileFormat(getArtifactsDir() + "Document.DigitalSignature.docx").hasDigitalSignature());

 // Please verify that all of the document's digital signatures are valid and check their details.
 Document signedDoc = new Document(getArtifactsDir() + "Document.DigitalSignature.docx");
 DigitalSignatureCollection digitalSignatureCollection = signedDoc.getDigitalSignatures();

 Assert.assertTrue(digitalSignatureCollection.isValid());
 Assert.assertEquals(1, digitalSignatureCollection.getCount());
 Assert.assertEquals(DigitalSignatureType.XML_DSIG, digitalSignatureCollection.get(0).getSignatureType());
 Assert.assertEquals("CN=Morzal.Me", signedDoc.getDigitalSignatures().get(0).getIssuerName());
 Assert.assertEquals("CN=Morzal.Me", signedDoc.getDigitalSignatures().get(0).getSubjectName());
 
```

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - The certificate holder object that contains the certificate was used to sign the document.
### getColorDepth() {#getColorDepth}
```
public int getColorDepth()
```


Получает глубину цвета для цифровой подписи.

**Returns:**
int — глубина цвета для цифровой подписи.
### getComments() {#getComments}
```
public String getComments()
```


Получает комментарий о цели подписи.

 **Examples:** 

Показывает, как проверять и отображать информацию о каждой подписи в документе.

```

 Document doc = new Document(getMyDir() + "Digitally signed.docx");

 for (DigitalSignature signature : doc.getDigitalSignatures()) {
     System.out.println("*** Signature Found ***");
     System.out.println("Is valid: " + signature.isValid());
     // This property is available in MS Word documents only
     System.out.println("Reason for signing: " + signature.getComments());
     System.out.println("Signature type: " + signature.getSignatureType());
     System.out.println("Time of signing: " + signature.getSignTime());
     System.out.println("Subject name: " + signature.getSubjectName());
     System.out.println("Issuer name: " + signature.getIssuerName());
     System.out.println();
 }
 
```

**Returns:**
java.lang.String - Комментарий цели подписи.
### getHorizontalResolution() {#getHorizontalResolution}
```
public int getHorizontalResolution()
```


Получает горизонтальное разрешение цифровой подписи.

**Returns:**
int — горизонтальное разрешение цифровой подписи.
### getIssuerName() {#getIssuerName}
```
public String getIssuerName()
```


Возвращает отличительное имя субъекта сертификата издателя.

 **Examples:** 

Показывает, как подписывать документы с помощью сертификатов X.509.

```

 // Verify that a document is not signed.
 Assert.assertFalse(FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx").hasDigitalSignature());

 // Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);

 SignOptions signOptions = new SignOptions();
 signOptions.setSignTime(new Date());

 // There are two ways of saving a signed copy of a document to the local file system:
 // 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "Document.DigitalSignature.docx",
         certificateHolder, signOptions);

 Assert.assertTrue(FileFormatUtil.detectFileFormat(getArtifactsDir() + "Document.DigitalSignature.docx").hasDigitalSignature());

 // 2 - Take a document from a stream, and save a signed copy to another stream.
 InputStream inDoc = new FileInputStream(getMyDir() + "Document.docx");
 try {
     OutputStream outDoc = new FileOutputStream(getArtifactsDir() + "Document.DigitalSignature.docx");
     try {
         DigitalSignatureUtil.sign(inDoc, outDoc, certificateHolder);
     } finally {
         if (outDoc != null) outDoc.close();
     }
 } finally {
     if (inDoc != null) inDoc.close();
 }

 Assert.assertTrue(FileFormatUtil.detectFileFormat(getArtifactsDir() + "Document.DigitalSignature.docx").hasDigitalSignature());

 // Please verify that all of the document's digital signatures are valid and check their details.
 Document signedDoc = new Document(getArtifactsDir() + "Document.DigitalSignature.docx");
 DigitalSignatureCollection digitalSignatureCollection = signedDoc.getDigitalSignatures();

 Assert.assertTrue(digitalSignatureCollection.isValid());
 Assert.assertEquals(1, digitalSignatureCollection.getCount());
 Assert.assertEquals(DigitalSignatureType.XML_DSIG, digitalSignatureCollection.get(0).getSignatureType());
 Assert.assertEquals("CN=Morzal.Me", signedDoc.getDigitalSignatures().get(0).getIssuerName());
 Assert.assertEquals("CN=Morzal.Me", signedDoc.getDigitalSignatures().get(0).getSubjectName());
 
```

**Returns:**
java.lang.String - Отличительное имя субъекта сертификата-издателя.
### getOfficeVersion() {#getOfficeVersion}
```
public String getOfficeVersion()
```


Получает версию Office для цифровой подписи.

**Returns:**
java.lang.String — версия Office для цифровой подписи.
### getSignTime() {#getSignTime}
```
public Date getSignTime()
```


Получает время подписи документа.

 **Examples:** 

Показывает, как проверять и отображать информацию о каждой подписи в документе.

```

 Document doc = new Document(getMyDir() + "Digitally signed.docx");

 for (DigitalSignature signature : doc.getDigitalSignatures()) {
     System.out.println("*** Signature Found ***");
     System.out.println("Is valid: " + signature.isValid());
     // This property is available in MS Word documents only
     System.out.println("Reason for signing: " + signature.getComments());
     System.out.println("Signature type: " + signature.getSignatureType());
     System.out.println("Time of signing: " + signature.getSignTime());
     System.out.println("Subject name: " + signature.getSubjectName());
     System.out.println("Issuer name: " + signature.getIssuerName());
     System.out.println();
 }
 
```

**Returns:**
java.util.Date - Время подписи документа.
### getSignatureType() {#getSignatureType}
```
public int getSignatureType()
```


Получает тип цифровой подписи.

 **Examples:** 

Показывает, как проверять и отображать информацию о каждой подписи в документе.

```

 Document doc = new Document(getMyDir() + "Digitally signed.docx");

 for (DigitalSignature signature : doc.getDigitalSignatures()) {
     System.out.println("*** Signature Found ***");
     System.out.println("Is valid: " + signature.isValid());
     // This property is available in MS Word documents only
     System.out.println("Reason for signing: " + signature.getComments());
     System.out.println("Signature type: " + signature.getSignatureType());
     System.out.println("Time of signing: " + signature.getSignTime());
     System.out.println("Subject name: " + signature.getSubjectName());
     System.out.println("Issuer name: " + signature.getIssuerName());
     System.out.println();
 }
 
```

**Returns:**
int - Тип цифровой подписи. Возвращаемое значение является одной из констант [DigitalSignatureType](../../com.aspose.words/digitalsignaturetype/).
### getSignatureValue() {#getSignatureValue}
```
public byte[] getSignatureValue()
```


Получает массив байтов, представляющих значение подписи.

 **Examples:** 

Показывает, как получить значение цифровой подписи из цифрово подписанного документа.

```

 Document doc = new Document(getMyDir() + "Digitally signed.docx");

 for (DigitalSignature digitalSignature : doc.getDigitalSignatures())
 {
     String signatureValue = Base64.getEncoder().encodeToString(digitalSignature.getSignatureValue());
     Assert.assertEquals("K1cVLLg2kbJRAzT5WK+m++G8eEO+l7S+5ENdjMxxTXkFzGUfvwxREuJdSFj9AbD" +
             "MhnGvDURv9KEhC25DDF1al8NRVR71TF3CjHVZXpYu7edQS5/yLw/k5CiFZzCp1+MmhOdYPcVO+Fm" +
             "+9fKr2iNLeyYB+fgEeZHfTqTFM2WwAqo=", signatureValue);
 }
 
```

**Returns:**
byte[] - Массив байтов, представляющих значение подписи.
### getSubjectName() {#getSubjectName}
```
public String getSubjectName()
```


Возвращает отличительное имя субъекта сертификата, который использовался для подписи документа.

 **Examples:** 

Показывает, как подписывать документы с помощью сертификатов X.509.

```

 // Verify that a document is not signed.
 Assert.assertFalse(FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx").hasDigitalSignature());

 // Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);

 SignOptions signOptions = new SignOptions();
 signOptions.setSignTime(new Date());

 // There are two ways of saving a signed copy of a document to the local file system:
 // 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "Document.DigitalSignature.docx",
         certificateHolder, signOptions);

 Assert.assertTrue(FileFormatUtil.detectFileFormat(getArtifactsDir() + "Document.DigitalSignature.docx").hasDigitalSignature());

 // 2 - Take a document from a stream, and save a signed copy to another stream.
 InputStream inDoc = new FileInputStream(getMyDir() + "Document.docx");
 try {
     OutputStream outDoc = new FileOutputStream(getArtifactsDir() + "Document.DigitalSignature.docx");
     try {
         DigitalSignatureUtil.sign(inDoc, outDoc, certificateHolder);
     } finally {
         if (outDoc != null) outDoc.close();
     }
 } finally {
     if (inDoc != null) inDoc.close();
 }

 Assert.assertTrue(FileFormatUtil.detectFileFormat(getArtifactsDir() + "Document.DigitalSignature.docx").hasDigitalSignature());

 // Please verify that all of the document's digital signatures are valid and check their details.
 Document signedDoc = new Document(getArtifactsDir() + "Document.DigitalSignature.docx");
 DigitalSignatureCollection digitalSignatureCollection = signedDoc.getDigitalSignatures();

 Assert.assertTrue(digitalSignatureCollection.isValid());
 Assert.assertEquals(1, digitalSignatureCollection.getCount());
 Assert.assertEquals(DigitalSignatureType.XML_DSIG, digitalSignatureCollection.get(0).getSignatureType());
 Assert.assertEquals("CN=Morzal.Me", signedDoc.getDigitalSignatures().get(0).getIssuerName());
 Assert.assertEquals("CN=Morzal.Me", signedDoc.getDigitalSignatures().get(0).getSubjectName());
 
```

**Returns:**
java.lang.String - Отличительное имя субъекта сертификата, который использовался для подписи документа.
### getVerticalResolution() {#getVerticalResolution}
```
public int getVerticalResolution()
```


Получает вертикальное разрешение цифровой подписи.

**Returns:**
int — вертикальное разрешение для цифровой подписи.
### getWindowsVersion() {#getWindowsVersion}
```
public String getWindowsVersion()
```


Получает версию Windows для цифровой подписи.

**Returns:**
java.lang.String — версия Windows для цифровой подписи.
### isValid() {#isValid}
```
public boolean isValid()
```


Возвращает  true  если эта цифровая подпись действительна и документ не был изменён.

 **Examples:** 

Показывает, как проверять и отображать информацию о каждой подписи в документе.

```

 Document doc = new Document(getMyDir() + "Digitally signed.docx");

 for (DigitalSignature signature : doc.getDigitalSignatures()) {
     System.out.println("*** Signature Found ***");
     System.out.println("Is valid: " + signature.isValid());
     // This property is available in MS Word documents only
     System.out.println("Reason for signing: " + signature.getComments());
     System.out.println("Signature type: " + signature.getSignatureType());
     System.out.println("Time of signing: " + signature.getSignTime());
     System.out.println("Subject name: " + signature.getSubjectName());
     System.out.println("Issuer name: " + signature.getIssuerName());
     System.out.println();
 }
 
```

**Returns:**
boolean -  true  если эта цифровая подпись действительна и документ не был изменён.
### toString() {#toString}
```
public String toString()
```


Возвращает удобочитаемую строку, отображающую значение этого объекта.

**Returns:**
java.lang.String
