---
title: CompressionLevel
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 88
url: /java/com.aspose.words/compressionlevel/
---

**Inheritance:**
java.lang.Object
```
public class CompressionLevel
```

A utility class providing constants. Compression level for OOXML files.

(DOCX and DOTX files are internally a ZIP-archive, this property controls the compression level of the archive.

Note, that FlatOpc file is not a ZIP-archive, therefore, this property does not affect the FlatOpc files.)
## Fields

| Field | Description |
| --- | --- |
| [NORMAL](#NORMAL) | Normal compression level. |
| [MAXIMUM](#MAXIMUM) | Maximum compression level. |
| [FAST](#FAST) | Fast compression level. |
| [SUPER_FAST](#SUPER-FAST) | Super Fast compression level. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int compressionLevel)](#getName-int-) |  |
| [toString(int compressionLevel)](#toString-int-) |  |
| [fromName(String compressionLevelName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### NORMAL {#NORMAL}
```
public static int NORMAL
```


Normal compression level. Default compression level used by Aspose.Words.

### MAXIMUM {#MAXIMUM}
```
public static int MAXIMUM
```


Maximum compression level.

### FAST {#FAST}
```
public static int FAST
```


Fast compression level.

### SUPER_FAST {#SUPER-FAST}
```
public static int SUPER_FAST
```


Super Fast compression level. Microsoft Word uses this compression level.

### length {#length}
```
public static int length
```


### getName(int compressionLevel) {#getName-int-}
```
public static String getName(int compressionLevel)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| compressionLevel | int |  |

**Returns:**
java.lang.String
### toString(int compressionLevel) {#toString-int-}
```
public static String toString(int compressionLevel)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| compressionLevel | int |  |

**Returns:**
java.lang.String
### fromName(String compressionLevelName) {#fromName-java.lang.String-}
```
public static int fromName(String compressionLevelName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| compressionLevelName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
