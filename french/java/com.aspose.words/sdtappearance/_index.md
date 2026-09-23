---
title: "SdtAppearance"
linktitle: "SdtAppearance"
second_title: "Aspose.Words pour Java"
description: "Spécifie l'apparence d'une balise de document structuré en Java."
type: docs
weight: 599
url: /fr/java/com.aspose.words/sdtappearance/
---

**Inheritance:**
java.lang.Object
```
public class SdtAppearance
```

Spécifie l'apparence d'une balise de document structuré.

 **Examples:** 

Montre comment afficher la balise autour du contenu.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [BOUNDING_BOX](#BOUNDING-BOX) | Représente une balise de document structuré affichée sous forme de rectangle ombré ou de boîte englobante. |
| [DEFAULT](#DEFAULT) | Par défaut, [BOUNDING\\_BOX](../../com.aspose.words/sdtappearance/\\#BOUNDING-BOX). |
| [HIDDEN](#HIDDEN) | Représente une balise de document structuré qui n'est pas affichée. |
| [TAGS](#TAGS) | Représente une balise de document structuré affichée sous forme de marqueurs de début et de fin. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String sdtAppearanceName)](#fromName-java.lang.String) |  |
| [getName(int sdtAppearance)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtAppearance)](#toString-int) |  |
### BOUNDING_BOX {#BOUNDING-BOX}
```
public static int BOUNDING_BOX
```


Représente une balise de document structuré affichée sous forme de rectangle ombré ou de boîte englobante.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Par défaut, [BOUNDING\\_BOX](../../com.aspose.words/sdtappearance/\\#BOUNDING-BOX).

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


Représente une balise de document structuré qui n'est pas affichée.

### TAGS {#TAGS}
```
public static int TAGS
```


Représente une balise de document structuré affichée sous forme de marqueurs de début et de fin.

### length {#length}
```
public static int length
```


### fromName(String sdtAppearanceName) {#fromName-java.lang.String}
```
public static int fromName(String sdtAppearanceName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sdtAppearanceName | java.lang.String |  |

**Returns:**
int
### getName(int sdtAppearance) {#getName-int}
```
public static String getName(int sdtAppearance)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| sdtAppearance | int |  |

**Returns:**
java.lang.String
