---
title: "SdtAppearance"
linktitle: "SdtAppearance"
second_title: "Aspose.Words per Java"
description: "Specifica l'aspetto di un tag di documento strutturato in Java."
type: docs
weight: 599
url: /it/java/com.aspose.words/sdtappearance/
---

**Inheritance:**
java.lang.Object
```
public class SdtAppearance
```

Specifica l'aspetto di un tag di documento strutturato.

 **Examples:** 

Mostra come visualizzare il tag attorno al contenuto.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [BOUNDING_BOX](#BOUNDING-BOX) | Rappresenta un tag di documento strutturato mostrato come un rettangolo ombreggiato o una casella di delimitazione. |
| [DEFAULT](#DEFAULT) | Il valore predefinito è [BOUNDING\_BOX](../../com.aspose.words/sdtappearance/\#BOUNDING-BOX). |
| [HIDDEN](#HIDDEN) | Rappresenta un tag di documento strutturato che non è visualizzato. |
| [TAGS](#TAGS) | Rappresenta un tag di documento strutturato mostrato come marcatori di inizio e fine. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String sdtAppearanceName)](#fromName-java.lang.String) |  |
| [getName(int sdtAppearance)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtAppearance)](#toString-int) |  |
### BOUNDING_BOX {#BOUNDING-BOX}
```
public static int BOUNDING_BOX
```


Rappresenta un tag di documento strutturato mostrato come un rettangolo ombreggiato o una casella di delimitazione.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Il valore predefinito è [BOUNDING\_BOX](../../com.aspose.words/sdtappearance/\#BOUNDING-BOX).

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


Rappresenta un tag di documento strutturato che non è visualizzato.

### TAGS {#TAGS}
```
public static int TAGS
```


Rappresenta un tag di documento strutturato mostrato come marcatori di inizio e fine.

### length {#length}
```
public static int length
```


### fromName(String sdtAppearanceName) {#fromName-java.lang.String}
```
public static int fromName(String sdtAppearanceName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sdtAppearanceName | java.lang.String |  |

**Returns:**
int
### getName(int sdtAppearance) {#getName-int}
```
public static String getName(int sdtAppearance)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sdtAppearance | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sdtAppearance) {#toString-int}
```
public static String toString(int sdtAppearance)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sdtAppearance | int |  |

**Returns:**
java.lang.String
