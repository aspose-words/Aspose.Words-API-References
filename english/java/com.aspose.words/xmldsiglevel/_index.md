---
title: XmlDsigLevel
linktitle: XmlDsigLevel
second_title: Aspose.Words for Java
description: Specifies the level of a digital signature based on XML-DSig standard in Java.
type: docs
weight: 748
url: /java/com.aspose.words/xmldsiglevel/
---

**Inheritance:**
java.lang.Object
```
public class XmlDsigLevel
```

Specifies the level of a digital signature based on XML-DSig standard.

 **Examples:** 

Shows how to sign document based on XML-DSig standard.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

Shows how to sign a document with timestamping using DigitalSignatureUtil.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_T);
     signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
             "https://freetsa.org/tsr",
             "JohnDoe",
             "MyPassword"));
 }

 CertificateHolder cert = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx");

 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signedDoc.getDigitalSignatures().get(0).isValid());

 // Verify timestamp settings are applied.
 Assert.assertEquals("https://freetsa.org/tsr", signOptions.getTimestampSettings().getServerUrl());
 Assert.assertEquals("JohnDoe", signOptions.getTimestampSettings().getUserName());
 Assert.assertEquals("MyPassword", signOptions.getTimestampSettings().getPassword());
 Assert.assertEquals(100.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());

 // Test with custom timeout.
 signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
         "https://freetsa.org/tsr",
         "JohnDoe",
         "MyPassword",
         Duration.ofMinutes(30)));

 Assert.assertEquals(1800.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());
 
```
## Fields

| Field | Description |
| --- | --- |
| [XML_D_SIG](#XML-D-SIG) | Specifies XML-DSig signature level. |
| [X_AD_ES_EPES](#X-AD-ES-EPES) | Specifies XAdES-EPES signature level. |
| [X_AD_ES_T](#X-AD-ES-T) | Specifies XAdES-T signature level. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String xmlDsigLevelName)](#fromName-java.lang.String) |  |
| [getName(int xmlDsigLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xmlDsigLevel)](#toString-int) |  |
### XML_D_SIG {#XML-D-SIG}
```
public static int XML_D_SIG
```


Specifies XML-DSig signature level.

 **Remarks:** 

A simple digital signature that should not be trusted after its signing certificate expires.

### X_AD_ES_EPES {#X-AD-ES-EPES}
```
public static int X_AD_ES_EPES
```


Specifies XAdES-EPES signature level.

 **Remarks:** 

Adds information about the signing certificate to the XML-DSig signature. A malicious user cannot switch the signing certificate for another certificate with the same public/private key.

### X_AD_ES_T {#X-AD-ES-T}
```
public static int X_AD_ES_T
```


Specifies XAdES-T signature level.

 **Remarks:** 

Adds an RFC 3161 timestamp of the signature value to the XAdES-EPES signature, obtained from a trusted timestamp authority (TSA). This proves the signature existed at a specific point in time, independent of the signing certificate's validity period.

### length {#length}
```
public static int length
```


### fromName(String xmlDsigLevelName) {#fromName-java.lang.String}
```
public static int fromName(String xmlDsigLevelName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xmlDsigLevelName | java.lang.String |  |

**Returns:**
int
### getName(int xmlDsigLevel) {#getName-int}
```
public static String getName(int xmlDsigLevel)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xmlDsigLevel | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int xmlDsigLevel) {#toString-int}
```
public static String toString(int xmlDsigLevel)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xmlDsigLevel | int |  |

**Returns:**
java.lang.String
