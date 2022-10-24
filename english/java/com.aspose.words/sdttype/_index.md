---
title: SdtType
second_title: Aspose.Words for Java API Reference
description: Specifies the type of a structured document tag SDT node.
type: docs
weight: 508
url: /java/com.aspose.words/sdttype/
---

**Inheritance:**
java.lang.Object
```
public class SdtType
```

Specifies the type of a structured document tag (SDT) node.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | No type is assigned to the SDT. |
| [BIBLIOGRAPHY](#BIBLIOGRAPHY) | The SDT represents a bibliography entry. |
| [CITATION](#CITATION) | The SDT represents a citation. |
| [EQUATION](#EQUATION) | The SDT represents an equation. |
| [DROP_DOWN_LIST](#DROP-DOWN-LIST) | The SDT represents a drop down list when displayed in the document. |
| [COMBO_BOX](#COMBO-BOX) | The SDT represents a combo box when displayed in the document. |
| [DATE](#DATE) | The SDT represents a date picker when displayed in the document. |
| [BUILDING_BLOCK_GALLERY](#BUILDING-BLOCK-GALLERY) | The SDT represents a building block gallery type. |
| [DOC_PART_OBJ](#DOC-PART-OBJ) | The SDT represents a document part type. |
| [GROUP](#GROUP) | The SDT represents a restricted grouping when displayed in the document. |
| [PICTURE](#PICTURE) | The SDT represents a picture when displayed in the document. |
| [RICH_TEXT](#RICH-TEXT) | The SDT represents a rich text box when displayed in the document. |
| [PLAIN_TEXT](#PLAIN-TEXT) | The SDT represents a plain text box when displayed in the document. |
| [CHECKBOX](#CHECKBOX) | The SDT represents a checkbox when displayed in the document. |
| [REPEATING_SECTION](#REPEATING-SECTION) | The SDT represents repeating section type when displayed in the document. |
| [REPEATING_SECTION_ITEM](#REPEATING-SECTION-ITEM) | The SDT represents repeating section item. |
| [ENTITY_PICKER](#ENTITY-PICKER) | The SDT represents an entity picker that allows the user to select an instance of an external content type. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int sdtType)](#getName-int-) |  |
| [toString(int sdtType)](#toString-int-) |  |
| [fromName(String sdtTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### NONE {#NONE}
```
public static int NONE
```


No type is assigned to the SDT.

### BIBLIOGRAPHY {#BIBLIOGRAPHY}
```
public static int BIBLIOGRAPHY
```


The SDT represents a bibliography entry.

### CITATION {#CITATION}
```
public static int CITATION
```


The SDT represents a citation.

### EQUATION {#EQUATION}
```
public static int EQUATION
```


The SDT represents an equation.

### DROP_DOWN_LIST {#DROP-DOWN-LIST}
```
public static int DROP_DOWN_LIST
```


The SDT represents a drop down list when displayed in the document.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


The SDT represents a combo box when displayed in the document.

### DATE {#DATE}
```
public static int DATE
```


The SDT represents a date picker when displayed in the document.

### BUILDING_BLOCK_GALLERY {#BUILDING-BLOCK-GALLERY}
```
public static int BUILDING_BLOCK_GALLERY
```


The SDT represents a building block gallery type.

### DOC_PART_OBJ {#DOC-PART-OBJ}
```
public static int DOC_PART_OBJ
```


The SDT represents a document part type.

### GROUP {#GROUP}
```
public static int GROUP
```


The SDT represents a restricted grouping when displayed in the document.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


The SDT represents a picture when displayed in the document.

### RICH_TEXT {#RICH-TEXT}
```
public static int RICH_TEXT
```


The SDT represents a rich text box when displayed in the document.

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


The SDT represents a plain text box when displayed in the document.

### CHECKBOX {#CHECKBOX}
```
public static int CHECKBOX
```


The SDT represents a checkbox when displayed in the document. This is MS-specific feature available since Office 2010 and not supported by the ISO/IEC 29500 OOXML standard.

### REPEATING_SECTION {#REPEATING-SECTION}
```
public static int REPEATING_SECTION
```


The SDT represents repeating section type when displayed in the document. This is MS-specific feature available since Office 2013 and not supported by the ISO/IEC 29500 OOXML standard.

### REPEATING_SECTION_ITEM {#REPEATING-SECTION-ITEM}
```
public static int REPEATING_SECTION_ITEM
```


The SDT represents repeating section item. This is MS-specific feature available since Office 2013 and not supported by the ISO/IEC 29500 OOXML standard.

### ENTITY_PICKER {#ENTITY-PICKER}
```
public static int ENTITY_PICKER
```


The SDT represents an entity picker that allows the user to select an instance of an external content type. This is MS-specific feature available since Office 2010 and not supported by the ISO/IEC 29500 OOXML standard.

### length {#length}
```
public static int length
```


### getName(int sdtType) {#getName-int-}
```
public static String getName(int sdtType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sdtType | int |  |

**Returns:**
java.lang.String
### toString(int sdtType) {#toString-int-}
```
public static String toString(int sdtType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sdtType | int |  |

**Returns:**
java.lang.String
### fromName(String sdtTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String sdtTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sdtTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
