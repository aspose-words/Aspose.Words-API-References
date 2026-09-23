---
title: "XmlDsigLevel"
linktitle: "XmlDsigLevel"
second_title: "Aspose.Words per Java"
description: "Specifica il livello di una firma digitale basata sullo standard XML-DSig in Java."
type: docs
weight: 747
url: /it/java/com.aspose.words/xmldsiglevel/
---

**Inheritance:**
java.lang.Object
```
public class XmlDsigLevel
```

Specifica il livello di una firma digitale basata sullo standard XML-DSig.

 **Examples:** 

Mostra come firmare un documento basato sullo standard XML-DSig.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [XML_D_SIG](#XML-D-SIG) | Specifica il livello della firma XML-DSig. |
| [X_AD_ES_EPES](#X-AD-ES-EPES) | Specifica il livello di firma XAdES-EPES. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String xmlDsigLevelName)](#fromName-java.lang.String) |  |
| [getName(int xmlDsigLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xmlDsigLevel)](#toString-int) |  |
### XML_D_SIG {#XML-D-SIG}
```
public static int XML_D_SIG
```


Specifica il livello della firma XML-DSig.

 **Remarks:** 

Una firma digitale semplice che non dovrebbe essere considerata affidabile dopo la scadenza del suo certificato di firma.

### X_AD_ES_EPES {#X-AD-ES-EPES}
```
public static int X_AD_ES_EPES
```


Specifica il livello di firma XAdES-EPES.

 **Remarks:** 

Aggiunge informazioni sul certificato di firma alla firma XML-DSig. Un utente malintenzionato non può sostituire il certificato di firma con un altro certificato con la stessa chiave pubblica/privata.

### length {#length}
```
public static int length
```


### fromName(String xmlDsigLevelName) {#fromName-java.lang.String}
```
public static int fromName(String xmlDsigLevelName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlDsigLevelName | java.lang.String |  |

**Returns:**
int
### getName(int xmlDsigLevel) {#getName-int}
```
public static String getName(int xmlDsigLevel)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlDsigLevel | int |  |

**Returns:**
java.lang.String
