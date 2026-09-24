---
title: "XmlDsigLevel"
linktitle: "XmlDsigLevel"
second_title: "Aspose.Words para Java"
description: "Especifica el nivel de una firma digital basado en el estándar XML-DSig en Java."
type: docs
weight: 747
url: /es/java/com.aspose.words/xmldsiglevel/
---

**Inheritance:**
java.lang.Object
```
public class XmlDsigLevel
```

Especifica el nivel de una firma digital basado en el estándar XML-DSig.

 **Examples:** 

Muestra cómo firmar un documento basado en el estándar XML-DSig.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [XML_D_SIG](#XML-D-SIG) | Especifica el nivel de firma XML-DSig. |
| [X_AD_ES_EPES](#X-AD-ES-EPES) | Especifica el nivel de firma XAdES-EPES. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String xmlDsigLevelName)](#fromName-java.lang.String) |  |
| [getName(int xmlDsigLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xmlDsigLevel)](#toString-int) |  |
### XML_D_SIG {#XML-D-SIG}
```
public static int XML_D_SIG
```


Especifica el nivel de firma XML-DSig.

 **Remarks:** 

Una firma digital simple que no debe confiarse después de que expire su certificado de firma.

### X_AD_ES_EPES {#X-AD-ES-EPES}
```
public static int X_AD_ES_EPES
```


Especifica el nivel de firma XAdES-EPES.

 **Remarks:** 

Agrega información sobre el certificado de firma a la firma XML-DSig. Un usuario malintencionado no puede cambiar el certificado de firma por otro certificado con la misma clave pública/privada.

### length {#length}
```
public static int length
```


### fromName(String xmlDsigLevelName) {#fromName-java.lang.String}
```
public static int fromName(String xmlDsigLevelName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xmlDsigLevelName | java.lang.String |  |

**Returns:**
int
### getName(int xmlDsigLevel) {#getName-int}
```
public static String getName(int xmlDsigLevel)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xmlDsigLevel | int |  |

**Returns:**
java.lang.String
