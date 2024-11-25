---
title: ReportBuildOptions
linktitle: ReportBuildOptions
second_title: Aspose.Words for Java
description: Specifies options controlling behavior of ReportingEngine while building a report in Java.
type: docs
weight: 538
url: /java/com.aspose.words/reportbuildoptions/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuildOptions
```

Specifies options controlling behavior of [ReportingEngine](../../com.aspose.words/reportingengine/) while building a report.
## Fields

| Field | Description |
| --- | --- |
| [ALLOW_MISSING_MEMBERS](#ALLOW-MISSING-MEMBERS) | Specifies that missing object members should be treated as null literals by the engine. |
| [INLINE_ERROR_MESSAGES](#INLINE-ERROR-MESSAGES) | Specifies that the engine should inline template syntax error messages into output documents. |
| [NONE](#NONE) | Specifies default options. |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | Specifies that the engine should remove paragraphs becoming empty after template syntax tags are removed or replaced with empty values. |
| [RESPECT_JPEG_EXIF_ORIENTATION](#RESPECT-JPEG-EXIF-ORIENTATION) | Specifies that the engine should use EXIF \\u200b\\u200bimage orientation values to appropriately rotate inserted JPEG images. |
| [UPDATE_FIELDS_SYNTAX_AWARE](#UPDATE-FIELDS-SYNTAX-AWARE) | Specifies that the engine should ignore template syntax in field results and update fields after a report is built. |
| [USE_LEGACY_HEADER_FOOTER_VISITING](#USE-LEGACY-HEADER-FOOTER-VISITING) | Specifies that the engine should visit section child nodes (headers, footers, bodies) in an order compatible with Aspose.Words versions prior 21.9. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String reportBuildOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set reportBuildOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int reportBuildOptions)](#getName-int) |  |
| [getNames(int reportBuildOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int reportBuildOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### ALLOW_MISSING_MEMBERS {#ALLOW-MISSING-MEMBERS}
```
public static int ALLOW_MISSING_MEMBERS
```


Specifies that missing object members should be treated as null literals by the engine. This option affects only access to instance (that is, non-static) object members and extension methods. If this option is not set, the engine throws an exception when encounters a missing object member.

### INLINE_ERROR_MESSAGES {#INLINE-ERROR-MESSAGES}
```
public static int INLINE_ERROR_MESSAGES
```


Specifies that the engine should inline template syntax error messages into output documents. If this option is not set, the engine throws an exception when encounters a syntax error.

### NONE {#NONE}
```
public static int NONE
```


Specifies default options.

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


Specifies that the engine should remove paragraphs becoming empty after template syntax tags are removed or replaced with empty values.

### RESPECT_JPEG_EXIF_ORIENTATION {#RESPECT-JPEG-EXIF-ORIENTATION}
```
public static int RESPECT_JPEG_EXIF_ORIENTATION
```


Specifies that the engine should use EXIF \\u200b\\u200bimage orientation values to appropriately rotate inserted JPEG images.

### UPDATE_FIELDS_SYNTAX_AWARE {#UPDATE-FIELDS-SYNTAX-AWARE}
```
public static int UPDATE_FIELDS_SYNTAX_AWARE
```


Specifies that the engine should ignore template syntax in field results and update fields after a report is built.

### USE_LEGACY_HEADER_FOOTER_VISITING {#USE-LEGACY-HEADER-FOOTER-VISITING}
```
public static int USE_LEGACY_HEADER_FOOTER_VISITING
```


Specifies that the engine should visit section child nodes (headers, footers, bodies) in an order compatible with Aspose.Words versions prior 21.9.

 **Remarks:** 

By default, the engine treats headers and footers as if they were linked to section breaks. That is, when visiting section child nodes, a body is visited first and only then, headers and footers are visited. This agrees with Microsoft Word behavior when copy-pasting or removing multi-section contents and produces more correct results in most scenarios.

Prior to Aspose.Words 21.9, the engine used another visiting order: Section child nodes were visited in an order they appear in a document. Apply this value to [ReportingEngine.getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [ReportingEngine.setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) if compatibility with older versions of Aspose.Words is required.

### length {#length}
```
public static int length
```


### fromName(String reportBuildOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String reportBuildOptionsName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| reportBuildOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set reportBuildOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set reportBuildOptionsNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| reportBuildOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int reportBuildOptions) {#getName-int}
```
public static String getName(int reportBuildOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.lang.String
### getNames(int reportBuildOptions) {#getNames-int}
```
public static Set getNames(int reportBuildOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int reportBuildOptions) {#toString-int}
```
public static String toString(int reportBuildOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
