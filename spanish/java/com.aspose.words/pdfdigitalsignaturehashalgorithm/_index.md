---
title: "PdfDigitalSignatureHashAlgorithm"
linktitle: "PdfDigitalSignatureHashAlgorithm"
second_title: "Aspose.Words para Java"
description: "Especifica un algoritmo de hash digital utilizado por una firma digital en Java."
type: docs
weight: 532
url: /es/java/com.aspose.words/pdfdigitalsignaturehashalgorithm/
---

**Inheritance:**
java.lang.Object
```
public class PdfDigitalSignatureHashAlgorithm
```

Especifica un algoritmo de hash digital utilizado por una firma digital.

 **Examples:** 

Muestra cómo firmar un documento PDF generado.

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
 Calendar calendar = Calendar.getInstance();
 calendar.set(2015, Calendar.JULY, 20);
 Date signingTime = calendar.getTime();
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime));
 options.getDigitalSignatureDetails().setHashAlgorithm(PdfDigitalSignatureHashAlgorithm.RIPE_MD_160);

 Assert.assertEquals(options.getDigitalSignatureDetails().getReason(), "Test Signing");
 Assert.assertEquals(options.getDigitalSignatureDetails().getLocation(), "My Office");
 Assert.assertEquals(DocumentHelper.getLocalDate(options.getDigitalSignatureDetails().getSignatureDate()), DocumentHelper.getLocalDate(signingTime));

 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [RIPE_MD_160](#RIPE-MD-160) | Algoritmo de hash RIPEMD-160. |
| [SHA_256](#SHA-256) | Algoritmo de hash SHA-256. |
| [SHA_384](#SHA-384) | Algoritmo de hash SHA-384. |
| [SHA_512](#SHA-512) | Algoritmo de hash SHA-512. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String pdfDigitalSignatureHashAlgorithmName)](#fromName-java.lang.String) |  |
| [getName(int pdfDigitalSignatureHashAlgorithm)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfDigitalSignatureHashAlgorithm)](#toString-int) |  |
### RIPE_MD_160 {#RIPE-MD-160}
```
public static int RIPE_MD_160
```


Algoritmo de hash RIPEMD-160.

### SHA_256 {#SHA-256}
```
public static int SHA_256
```


Algoritmo de hash SHA-256.

### SHA_384 {#SHA-384}
```
public static int SHA_384
```


Algoritmo de hash SHA-384.

### SHA_512 {#SHA-512}
```
public static int SHA_512
```


Algoritmo de hash SHA-512.

### length {#length}
```
public static int length
```


### fromName(String pdfDigitalSignatureHashAlgorithmName) {#fromName-java.lang.String}
```
public static int fromName(String pdfDigitalSignatureHashAlgorithmName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfDigitalSignatureHashAlgorithmName | java.lang.String |  |

**Returns:**
int
### getName(int pdfDigitalSignatureHashAlgorithm) {#getName-int}
```
public static String getName(int pdfDigitalSignatureHashAlgorithm)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfDigitalSignatureHashAlgorithm | int |  |

**Returns:**
java.lang.String
