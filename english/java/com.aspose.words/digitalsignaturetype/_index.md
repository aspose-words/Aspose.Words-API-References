---
title: DigitalSignatureType
linktitle: DigitalSignatureType
second_title: Aspose.Words for Java
description: Specifies the type of a digital signature in Java.
type: docs
weight: 134
url: /java/com.aspose.words/digitalsignaturetype/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignatureType
```

Specifies the type of a digital signature.

 **Examples:** 

Shows how to sign documents with X.509 certificates.

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
## Fields

| Field | Description |
| --- | --- |
| [CRYPTO_API](#CRYPTO-API) | The Crypto API signature method used in Microsoft Word 97-2003 .DOC binary documents. |
| [UNKNOWN](#UNKNOWN) | Indicates an error, unknown digital signature type. |
| [XML_DSIG](#XML-DSIG) | The XmlDsig signature method used in OOXML and OpenDocument documents. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String digitalSignatureTypeName)](#fromName-java.lang.String) |  |
| [getName(int digitalSignatureType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int digitalSignatureType)](#toString-int) |  |
### CRYPTO_API {#CRYPTO-API}
```
public static int CRYPTO_API
```


The Crypto API signature method used in Microsoft Word 97-2003 .DOC binary documents.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Indicates an error, unknown digital signature type.

### XML_DSIG {#XML-DSIG}
```
public static int XML_DSIG
```


The XmlDsig signature method used in OOXML and OpenDocument documents.

### length {#length}
```
public static int length
```


### fromName(String digitalSignatureTypeName) {#fromName-java.lang.String}
```
public static int fromName(String digitalSignatureTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| digitalSignatureTypeName | java.lang.String |  |

**Returns:**
int
### getName(int digitalSignatureType) {#getName-int}
```
public static String getName(int digitalSignatureType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| digitalSignatureType | int |  |

**Returns:**
java.lang.String
