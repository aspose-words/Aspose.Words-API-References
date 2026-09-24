---
title: "XmlDsigLevel"
linktitle: "XmlDsigLevel"
second_title: "Aspose.Words Java için"
description: "Java'da XML-DSig standardına dayalı bir dijital imzanın seviyesini belirtir."
type: docs
weight: 747
url: /tr/java/com.aspose.words/xmldsiglevel/
---

**Inheritance:**
java.lang.Object
```
public class XmlDsigLevel
```

XML-DSig standardına dayalı bir dijital imzanın seviyesini belirtir.

 **Examples:** 

XML-DSig standardına dayalı belgeyi nasıl imzalayacağınızı gösterir.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [XML_D_SIG](#XML-D-SIG) | XML-DSig imza seviyesini belirtir. |
| [X_AD_ES_EPES](#X-AD-ES-EPES) | XAdES-EPES imza seviyesini belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String xmlDsigLevelName)](#fromName-java.lang.String) |  |
| [getName(int xmlDsigLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xmlDsigLevel)](#toString-int) |  |
### XML_D_SIG {#XML-D-SIG}
```
public static int XML_D_SIG
```


XML-DSig imza seviyesini belirtir.

 **Remarks:** 

İmza sertifikası süresi dolduktan sonra güvenilmemesi gereken basit bir dijital imza.

### X_AD_ES_EPES {#X-AD-ES-EPES}
```
public static int X_AD_ES_EPES
```


XAdES-EPES imza seviyesini belirtir.

 **Remarks:** 

İmza sertifikası hakkında bilgiyi XML-DSig imzasına ekler. Kötü niyetli bir kullanıcı aynı açık/özel anahtara sahip başka bir sertifika ile imza sertifikasını değiştiremez.

### length {#length}
```
public static int length
```


### fromName(String xmlDsigLevelName) {#fromName-java.lang.String}
```
public static int fromName(String xmlDsigLevelName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xmlDsigLevelName | java.lang.String |  |

**Returns:**
int
### getName(int xmlDsigLevel) {#getName-int}
```
public static String getName(int xmlDsigLevel)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xmlDsigLevel | int |  |

**Returns:**
java.lang.String
