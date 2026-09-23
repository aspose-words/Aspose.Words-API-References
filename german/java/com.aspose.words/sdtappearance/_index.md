---
title: "SdtAppearance"
linktitle: "SdtAppearance"
second_title: "Aspose.Words für Java"
description: "Gibt das Aussehen eines strukturierten Dokumenten‑Tags in Java an."
type: docs
weight: 599
url: /de/java/com.aspose.words/sdtappearance/
---

**Inheritance:**
java.lang.Object
```
public class SdtAppearance
```

Legt das Erscheinungsbild eines strukturierten Dokumenttags fest.

 **Examples:** 

Zeigt, wie man ein Tag um den Inhalt herum anzeigt.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BOUNDING_BOX](#BOUNDING-BOX) | Stellt ein strukturiertes Dokumenten‑Tag dar, das als schattiertes Rechteck oder Begrenzungsrahmen angezeigt wird. |
| [DEFAULT](#DEFAULT) | Standardwert ist [BOUNDING\_BOX](../../com.aspose.words/sdtappearance/\#BOUNDING-BOX). |
| [HIDDEN](#HIDDEN) | Stellt ein strukturiertes Dokumenten‑Tag dar, das nicht angezeigt wird. |
| [TAGS](#TAGS) | Stellt ein strukturiertes Dokumenten‑Tag dar, das als Anfangs‑ und End‑Markierungen angezeigt wird. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String sdtAppearanceName)](#fromName-java.lang.String) |  |
| [getName(int sdtAppearance)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtAppearance)](#toString-int) |  |
### BOUNDING_BOX {#BOUNDING-BOX}
```
public static int BOUNDING_BOX
```


Stellt ein strukturiertes Dokumenten‑Tag dar, das als schattiertes Rechteck oder Begrenzungsrahmen angezeigt wird.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Standardwert ist [BOUNDING\_BOX](../../com.aspose.words/sdtappearance/\#BOUNDING-BOX).

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


Stellt ein strukturiertes Dokumenten‑Tag dar, das nicht angezeigt wird.

### TAGS {#TAGS}
```
public static int TAGS
```


Stellt ein strukturiertes Dokumenten‑Tag dar, das als Anfangs‑ und End‑Markierungen angezeigt wird.

### length {#length}
```
public static int length
```


### fromName(String sdtAppearanceName) {#fromName-java.lang.String}
```
public static int fromName(String sdtAppearanceName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sdtAppearanceName | java.lang.String |  |

**Returns:**
int
### getName(int sdtAppearance) {#getName-int}
```
public static String getName(int sdtAppearance)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sdtAppearance | int |  |

**Returns:**
java.lang.String
