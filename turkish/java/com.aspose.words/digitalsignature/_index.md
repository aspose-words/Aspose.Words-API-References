---
title: "DigitalSignature"
linktitle: "DigitalSignature"
second_title: "Aspose.Words Java için"
description: "Java'da bir belgedeki dijital imzayı ve doğrulama sonucunu temsil eder."
type: docs
weight: 150
url: /tr/java/com.aspose.words/digitalsignature/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignature
```

Bir belgedeki dijital imzayı ve doğrulama sonucunu temsil eder.

Daha fazla bilgi için, [ Work with Digital Signatures ][Work with Digital Signatures] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir belgede her imzanın nasıl doğrulanacağını ve bilgilerin nasıl görüntüleneceğini gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getApplicationVersion()](#getApplicationVersion) | Dijital imza için uygulama sürümünü alır. |
| [getCertificateHolder()](#getCertificateHolder) | Belgeyi imzalamak için kullanılan sertifikayı içeren sertifika sahibi nesnesini döndürür. |
| [getColorDepth()](#getColorDepth) | Dijital imza için renk derinliğini alır. |
| [getComments()](#getComments) | İmza amacının yorumunu alır. |
| [getHorizontalResolution()](#getHorizontalResolution) | Dijital imza için yatay çözünürlüğü alır. |
| [getIssuerName()](#getIssuerName) | Sertifika verenin konu ayırt edici adını döndürür. |
| [getOfficeVersion()](#getOfficeVersion) | Dijital imza için Office sürümünü alır. |
| [getSignTime()](#getSignTime) | Belgenin imzalanma zamanını alır. |
| [getSignatureType()](#getSignatureType) | Dijital imzanın türünü alır. |
| [getSignatureValue()](#getSignatureValue) | İmza değerini temsil eden bir bayt dizisini alır. |
| [getSubjectName()](#getSubjectName) | Belgeyi imzalamak için kullanılan sertifikanın konu ayırt edici adını döndürür. |
| [getVerticalResolution()](#getVerticalResolution) | Dijital imza için dikey çözünürlüğü alır. |
| [getWindowsVersion()](#getWindowsVersion) | Dijital imza için Windows sürümünü alır. |
| [isValid()](#isValid) | Bu dijital imza geçerli ve belge değiştirilmemişse  true  değerini döndürür. |
| [toString()](#toString) | Bu nesnenin değerini gösteren kullanıcı dostu bir dize döndürür. |
### getApplicationVersion() {#getApplicationVersion}
```
public String getApplicationVersion()
```


Dijital imza için uygulama sürümünü alır.

**Returns:**
java.lang.String - Dijital imza için uygulama sürümü.
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Belgeyi imzalamak için kullanılan sertifikayı içeren sertifika sahibi nesnesini döndürür.

 **Examples:** 

X.509 sertifikalarıyla belgelerin nasıl imzalanacağını gösterir.

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


Dijital imza için renk derinliğini alır.

**Returns:**
int - Dijital imza için renk derinliği.
### getComments() {#getComments}
```
public String getComments()
```


İmza amacının yorumunu alır.

 **Examples:** 

Bir belgede her imzanın nasıl doğrulanacağını ve bilgilerin nasıl görüntüleneceğini gösterir.

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
java.lang.String - İmzalama amacı yorumu.
### getHorizontalResolution() {#getHorizontalResolution}
```
public int getHorizontalResolution()
```


Dijital imza için yatay çözünürlüğü alır.

**Returns:**
int - Dijital imza için yatay çözünürlük.
### getIssuerName() {#getIssuerName}
```
public String getIssuerName()
```


Sertifika verenin konu ayırt edici adını döndürür.

 **Examples:** 

X.509 sertifikalarıyla belgelerin nasıl imzalanacağını gösterir.

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
java.lang.String - Sertifika verenin konu ayırt edici adı.
### getOfficeVersion() {#getOfficeVersion}
```
public String getOfficeVersion()
```


Dijital imza için Office sürümünü alır.

**Returns:**
java.lang.String - Dijital imza için Office sürümü.
### getSignTime() {#getSignTime}
```
public Date getSignTime()
```


Belgenin imzalanma zamanını alır.

 **Examples:** 

Bir belgede her imzanın nasıl doğrulanacağını ve bilgilerin nasıl görüntüleneceğini gösterir.

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
java.util.Date - Belgenin imzalandığı zaman.
### getSignatureType() {#getSignatureType}
```
public int getSignatureType()
```


Dijital imzanın türünü alır.

 **Examples:** 

Bir belgede her imzanın nasıl doğrulanacağını ve bilgilerin nasıl görüntüleneceğini gösterir.

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
int - Dijital imzanın türü. Döndürülen değer, [DigitalSignatureType](../../com.aspose.words/digitalsignaturetype/) sabitlerinden biridir.
### getSignatureValue() {#getSignatureValue}
```
public byte[] getSignatureValue()
```


İmza değerini temsil eden bir bayt dizisini alır.

 **Examples:** 

Dijital olarak imzalanmış bir belgeden dijital imza değerinin nasıl alınacağını gösterir.

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
byte[] - İmza değerini temsil eden bir bayt dizisi.
### getSubjectName() {#getSubjectName}
```
public String getSubjectName()
```


Belgeyi imzalamak için kullanılan sertifikanın konu ayırt edici adını döndürür.

 **Examples:** 

X.509 sertifikalarıyla belgelerin nasıl imzalanacağını gösterir.

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
java.lang.String - Belgeyi imzalamak için kullanılan sertifikanın konu ayırt edici adı.
### getVerticalResolution() {#getVerticalResolution}
```
public int getVerticalResolution()
```


Dijital imza için dikey çözünürlüğü alır.

**Returns:**
int - Dijital imza için dikey çözünürlük.
### getWindowsVersion() {#getWindowsVersion}
```
public String getWindowsVersion()
```


Dijital imza için Windows sürümünü alır.

**Returns:**
java.lang.String - Dijital imza için Windows sürümü.
### isValid() {#isValid}
```
public boolean isValid()
```


Bu dijital imza geçerli ve belge değiştirilmemişse  true  değerini döndürür.

 **Examples:** 

Bir belgede her imzanın nasıl doğrulanacağını ve bilgilerin nasıl görüntüleneceğini gösterir.

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
boolean -  true  bu dijital imza geçerli ve belge değiştirilmemişse.
### toString() {#toString}
```
public String toString()
```


Bu nesnenin değerini gösteren kullanıcı dostu bir dize döndürür.

**Returns:**
java.lang.String
