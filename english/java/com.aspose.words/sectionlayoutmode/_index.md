---
title: SectionLayoutMode
second_title: Aspose.Words for Java API Reference
description: Specifies the layout mode for a section allowing to define the document grid behavior.
type: docs
weight: 511
url: /java/com.aspose.words/sectionlayoutmode/
---

**Inheritance:**
java.lang.Object
```
public class SectionLayoutMode
```

Specifies the layout mode for a section allowing to define the document grid behavior.
## Fields

| Field | Description |
| --- | --- |
| [DEFAULT](#DEFAULT) | Specifies that no document grid shall be applied to the contents of the corresponding section in the document. |
| [GRID](#GRID) | Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line. |
| [LINE_GRID](#LINE-GRID) | Specifies that the corresponding section shall have additional line pitch added to each line within it in order to maintain the specified number of lines per page. |
| [SNAP_TO_CHARS](#SNAP-TO-CHARS) | Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int sectionLayoutMode)](#getName-int-) |  |
| [toString(int sectionLayoutMode)](#toString-int-) |  |
| [fromName(String sectionLayoutModeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Specifies that no document grid shall be applied to the contents of the corresponding section in the document.

### GRID {#GRID}
```
public static int GRID
```


Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line. Characters will not be automatically aligned with gridlines on typing.

### LINE_GRID {#LINE-GRID}
```
public static int LINE_GRID
```


Specifies that the corresponding section shall have additional line pitch added to each line within it in order to maintain the specified number of lines per page.

### SNAP_TO_CHARS {#SNAP-TO-CHARS}
```
public static int SNAP_TO_CHARS
```


Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line. Characters will be automatically aligned with gridlines on typing.

### length {#length}
```
public static int length
```


### getName(int sectionLayoutMode) {#getName-int-}
```
public static String getName(int sectionLayoutMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sectionLayoutMode | int |  |

**Returns:**
java.lang.String
### toString(int sectionLayoutMode) {#toString-int-}
```
public static String toString(int sectionLayoutMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sectionLayoutMode | int |  |

**Returns:**
java.lang.String
### fromName(String sectionLayoutModeName) {#fromName-java.lang.String-}
```
public static int fromName(String sectionLayoutModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sectionLayoutModeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
