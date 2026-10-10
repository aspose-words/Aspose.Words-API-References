---
title: "XmlDsigLevel"
linktitle: "XmlDsigLevel"
second_title: "Aspose.Words pour Java"
description: "Spécifie le niveau d'une signature numérique basé sur la norme XML-DSig en Java."
type: docs
weight: 747
url: /fr/java/com.aspose.words/xmldsiglevel/
---

**Inheritance:**
java.lang.Object
```
public class XmlDsigLevel
```

Spécifie le niveau d'une signature numérique basé sur la norme XML-DSig.

 **Examples:** 

Montre comment signer un document basé sur la norme XML-DSig.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [XML_D_SIG](#XML-D-SIG) | Spécifie le niveau de signature XML-DSig. |
| [X_AD_ES_EPES](#X-AD-ES-EPES) | Spécifie le niveau de signature XAdES-EPES. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String xmlDsigLevelName)](#fromName-java.lang.String) |  |
| [getName(int xmlDsigLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xmlDsigLevel)](#toString-int) |  |
### XML_D_SIG {#XML-D-SIG}
```
public static int XML_D_SIG
```


Spécifie le niveau de signature XML-DSig.

 **Remarks:** 

Une signature numérique simple qui ne doit pas être fiable après l'expiration de son certificat de signature.

### X_AD_ES_EPES {#X-AD-ES-EPES}
```
public static int X_AD_ES_EPES
```


Spécifie le niveau de signature XAdES-EPES.

 **Remarks:** 

Ajoute des informations sur le certificat de signature à la signature XML-DSig. Un utilisateur malveillant ne peut pas remplacer le certificat de signature par un autre certificat avec la même clé publique/privée.

### length {#length}
```
public static int length
```


### fromName(String xmlDsigLevelName) {#fromName-java.lang.String}
```
public static int fromName(String xmlDsigLevelName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| xmlDsigLevelName | java.lang.String |  |

**Returns:**
int
### getName(int xmlDsigLevel) {#getName-int}
```
public static String getName(int xmlDsigLevel)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| xmlDsigLevel | int |  |

**Returns:**
java.lang.String
