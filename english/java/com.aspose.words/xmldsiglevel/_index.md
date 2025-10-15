---
title: XmlDsigLevel
linktitle: XmlDsigLevel
second_title: Aspose.Words for Java
description: Specifies the level of a digital signature based on XML-DSig standard in Java.
type: docs
weight: 743
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
## Fields

| Field | Description |
| --- | --- |
| [XML_D_SIG](#XML-D-SIG) | Specifies XML-DSig signature level. |
| [X_AD_ES_EPES](#X-AD-ES-EPES) | Specifies XAdES-EPES signature level. |
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
