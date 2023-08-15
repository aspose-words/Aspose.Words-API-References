---
title: PdfDigitalSignatureHashAlgorithm
linktitle: PdfDigitalSignatureHashAlgorithm
second_title: Aspose.Words for Java
description: Specifies a digital hash algorithm used by a digital signature in Java.
type: docs
weight: 473
url: /java/com.aspose.words/pdfdigitalsignaturehashalgorithm/
---

**Inheritance:**
java.lang.Object
```
public class PdfDigitalSignatureHashAlgorithm
```

Specifies a digital hash algorithm used by a digital signature.

 **Examples:** 

Shows how to sign a generated PDF document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Contents of signed PDF.");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
 // digitally sign the document as we render it with the "Save" method.
 Date signingTime = new Date();
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime));
 options.getDigitalSignatureDetails().setHashAlgorithm(PdfDigitalSignatureHashAlgorithm.RIPE_MD_160);

 Assert.assertEquals(options.getDigitalSignatureDetails().getReason(), "Test Signing");
 Assert.assertEquals(options.getDigitalSignatureDetails().getLocation(), "My Office");
 Assert.assertEquals(options.getDigitalSignatureDetails().getSignatureDate(), signingTime);

 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
 
```
## Fields

| Field | Description |
| --- | --- |
| [RIPE_MD_160](#RIPE-MD-160) | RIPEMD-160 hash algorithm. |
| [SHA_256](#SHA-256) | SHA-256 hash algorithm. |
| [SHA_384](#SHA-384) | SHA-384 hash algorithm. |
| [SHA_512](#SHA-512) | SHA-512 hash algorithm. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String pdfDigitalSignatureHashAlgorithmName)](#fromName-java.lang.String) |  |
| [getName(int pdfDigitalSignatureHashAlgorithm)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfDigitalSignatureHashAlgorithm)](#toString-int) |  |
### RIPE_MD_160 {#RIPE-MD-160}
```
public static int RIPE_MD_160
```


RIPEMD-160 hash algorithm.

### SHA_256 {#SHA-256}
```
public static int SHA_256
```


SHA-256 hash algorithm.

### SHA_384 {#SHA-384}
```
public static int SHA_384
```


SHA-384 hash algorithm.

### SHA_512 {#SHA-512}
```
public static int SHA_512
```


SHA-512 hash algorithm.

### length {#length}
```
public static int length
```


### fromName(String pdfDigitalSignatureHashAlgorithmName) {#fromName-java.lang.String}
```
public static int fromName(String pdfDigitalSignatureHashAlgorithmName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfDigitalSignatureHashAlgorithmName | java.lang.String |  |

**Returns:**
int
### getName(int pdfDigitalSignatureHashAlgorithm) {#getName-int}
```
public static String getName(int pdfDigitalSignatureHashAlgorithm)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfDigitalSignatureHashAlgorithm | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfDigitalSignatureHashAlgorithm) {#toString-int}
```
public static String toString(int pdfDigitalSignatureHashAlgorithm)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfDigitalSignatureHashAlgorithm | int |  |

**Returns:**
java.lang.String
