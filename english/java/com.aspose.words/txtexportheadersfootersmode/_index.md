---
title: TxtExportHeadersFootersMode
second_title: Aspose.Words for Java API Reference
description: Specifies the way headers and footers are exported to plain text format.
type: docs
weight: 581
url: /java/com.aspose.words/txtexportheadersfootersmode/
---

**Inheritance:**
java.lang.Object
```
public class TxtExportHeadersFootersMode
```

Specifies the way headers and footers are exported to plain text format.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | No headers and footers are exported. |
| [PRIMARY_ONLY](#PRIMARY-ONLY) | Only primary headers and footers are exported at the beginning and end of each section. |
| [ALL_AT_END](#ALL-AT-END) | All headers and footers are placed after all section bodies at the very end of a document. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int txtExportHeadersFootersMode)](#getName-int-) |  |
| [toString(int txtExportHeadersFootersMode)](#toString-int-) |  |
| [fromName(String txtExportHeadersFootersModeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### NONE {#NONE}
```
public static int NONE
```


No headers and footers are exported.

### PRIMARY_ONLY {#PRIMARY-ONLY}
```
public static int PRIMARY_ONLY
```


Only primary headers and footers are exported at the beginning and end of each section.

It is hard to meaningfully output headers and footers to plain text because it is not paginated.

When this mode is used, only primary headers and footers are exported at the beginning and end of each section.

### ALL_AT_END {#ALL-AT-END}
```
public static int ALL_AT_END
```


All headers and footers are placed after all section bodies at the very end of a document. This mode is similar to Word.

### length {#length}
```
public static int length
```


### getName(int txtExportHeadersFootersMode) {#getName-int-}
```
public static String getName(int txtExportHeadersFootersMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| txtExportHeadersFootersMode | int |  |

**Returns:**
java.lang.String
### toString(int txtExportHeadersFootersMode) {#toString-int-}
```
public static String toString(int txtExportHeadersFootersMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| txtExportHeadersFootersMode | int |  |

**Returns:**
java.lang.String
### fromName(String txtExportHeadersFootersModeName) {#fromName-java.lang.String-}
```
public static int fromName(String txtExportHeadersFootersModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| txtExportHeadersFootersModeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
