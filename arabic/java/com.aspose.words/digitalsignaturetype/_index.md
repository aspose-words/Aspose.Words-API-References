---
title: "DigitalSignatureType"
linktitle: "DigitalSignatureType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع التوقيع الرقمي في Java."
type: docs
weight: 153
url: /ar/java/com.aspose.words/digitalsignaturetype/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignatureType
```

يحدد نوع التوقيع الرقمي.

 **Examples:** 

يعرض كيفية توقيع المستندات باستخدام شهادات X.509.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [CRYPTO_API](#CRYPTO-API) | طريقة توقيع Crypto API المستخدمة في مستندات .DOC الثنائية في Microsoft Word 97-2003. |
| [UNKNOWN](#UNKNOWN) | يشير إلى خطأ، نوع توقيع رقمي غير معروف. |
| [XML_DSIG](#XML-DSIG) | طريقة توقيع XmlDsig المستخدمة في مستندات OOXML و OpenDocument. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String digitalSignatureTypeName)](#fromName-java.lang.String) |  |
| [getName(int digitalSignatureType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int digitalSignatureType)](#toString-int) |  |
### CRYPTO_API {#CRYPTO-API}
```
public static int CRYPTO_API
```


طريقة توقيع Crypto API المستخدمة في مستندات .DOC الثنائية في Microsoft Word 97-2003.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


يشير إلى خطأ، نوع توقيع رقمي غير معروف.

### XML_DSIG {#XML-DSIG}
```
public static int XML_DSIG
```


طريقة توقيع XmlDsig المستخدمة في مستندات OOXML و OpenDocument.

### length {#length}
```
public static int length
```


### fromName(String digitalSignatureTypeName) {#fromName-java.lang.String}
```
public static int fromName(String digitalSignatureTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| digitalSignatureTypeName | java.lang.String |  |

**Returns:**
int
### getName(int digitalSignatureType) {#getName-int}
```
public static String getName(int digitalSignatureType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| digitalSignatureType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int digitalSignatureType) {#toString-int}
```
public static String toString(int digitalSignatureType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| digitalSignatureType | int |  |

**Returns:**
java.lang.String
