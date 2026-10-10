---
title: "XmlDsigLevel"
linktitle: "XmlDsigLevel"
second_title: "Aspose.Words für Java"
description: "Gibt das Niveau einer digitalen Signatur basierend auf dem XML-DSig-Standard in Java an."
type: docs
weight: 747
url: /de/java/com.aspose.words/xmldsiglevel/
---

**Inheritance:**
java.lang.Object
```
public class XmlDsigLevel
```

Gibt das Niveau einer digitalen Signatur basierend auf dem XML-DSig-Standard an.

 **Examples:** 

Zeigt, wie man ein Dokument basierend auf dem XML-DSig‑Standard signiert.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [XML_D_SIG](#XML-D-SIG) | Gibt das XML-DSig-Signaturniveau an. |
| [X_AD_ES_EPES](#X-AD-ES-EPES) | Gibt das XAdES-EPES-Signaturniveau an. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String xmlDsigLevelName)](#fromName-java.lang.String) |  |
| [getName(int xmlDsigLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xmlDsigLevel)](#toString-int) |  |
### XML_D_SIG {#XML-D-SIG}
```
public static int XML_D_SIG
```


Gibt das XML-DSig-Signaturniveau an.

 **Remarks:** 

Eine einfache digitale Signatur, die nach Ablauf ihres Signaturzertifikats nicht mehr vertrauenswürdig sein sollte.

### X_AD_ES_EPES {#X-AD-ES-EPES}
```
public static int X_AD_ES_EPES
```


Gibt das XAdES-EPES-Signaturniveau an.

 **Remarks:** 

Fügt der XML-DSig-Signatur Informationen über das Signaturzertifikat hinzu. Ein böswilliger Benutzer kann das Signaturzertifikat nicht gegen ein anderes Zertifikat mit demselben öffentlichen/privaten Schlüssel austauschen.

### length {#length}
```
public static int length
```


### fromName(String xmlDsigLevelName) {#fromName-java.lang.String}
```
public static int fromName(String xmlDsigLevelName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlDsigLevelName | java.lang.String |  |

**Returns:**
int
### getName(int xmlDsigLevel) {#getName-int}
```
public static String getName(int xmlDsigLevel)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlDsigLevel | int |  |

**Returns:**
java.lang.String
