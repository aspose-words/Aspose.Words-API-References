---
title: TxtLoadOptions
second_title: Aspose.Words for Java API Reference
description: Allows to specify additional options when loading  document into a  object.
type: docs
weight: 584
url: /java/com.aspose.words/txtloadoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions)
```
public class TxtLoadOptions extends LoadOptions
```

Allows to specify additional options when loading [LoadFormat.TEXT](../../com.aspose.words/loadformat\#TEXT) document into a [Document](../../com.aspose.words/document) object.

To learn more, visit the **Specify Load Options** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [TxtLoadOptions()](#TxtLoadOptions--) | Initializes a new instance of this class with default values. |
## Methods

| Method | Description |
| --- | --- |
| [getAutoNumberingDetection()](#getAutoNumberingDetection--) | Gets a boolean value indicating either automatic numbering detection will be performed while loading a document. |
| [setAutoNumberingDetection(boolean value)](#setAutoNumberingDetection-boolean-) | Sets a boolean value indicating either automatic numbering detection will be performed while loading a document. |
| [getDetectNumberingWithWhitespaces()](#getDetectNumberingWithWhitespaces--) | Allows to specify how numbered list items are recognized when document is imported from plain text format. |
| [setDetectNumberingWithWhitespaces(boolean value)](#setDetectNumberingWithWhitespaces-boolean-) | Allows to specify how numbered list items are recognized when document is imported from plain text format. |
| [getTrailingSpacesOptions()](#getTrailingSpacesOptions--) | Gets preferred option of a trailing space handling. |
| [setTrailingSpacesOptions(int value)](#setTrailingSpacesOptions-int-) | Sets preferred option of a trailing space handling. |
| [getLeadingSpacesOptions()](#getLeadingSpacesOptions--) | Gets preferred option of a leading space handling. |
| [setLeadingSpacesOptions(int value)](#setLeadingSpacesOptions-int-) | Sets preferred option of a leading space handling. |
| [getDocumentDirection()](#getDocumentDirection--) | Gets a document direction. |
| [setDocumentDirection(int value)](#setDocumentDirection-int-) | Sets a document direction. |
### TxtLoadOptions() {#TxtLoadOptions--}
```
public TxtLoadOptions()
```


Initializes a new instance of this class with default values.

### getAutoNumberingDetection() {#getAutoNumberingDetection--}
```
public boolean getAutoNumberingDetection()
```


Gets a boolean value indicating either automatic numbering detection will be performed while loading a document. The default value is  true .

**Returns:**
boolean - A boolean value indicating either automatic numbering detection will be performed while loading a document.
### setAutoNumberingDetection(boolean value) {#setAutoNumberingDetection-boolean-}
```
public void setAutoNumberingDetection(boolean value)
```


Sets a boolean value indicating either automatic numbering detection will be performed while loading a document. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating either automatic numbering detection will be performed while loading a document. |

### getDetectNumberingWithWhitespaces() {#getDetectNumberingWithWhitespaces--}
```
public boolean getDetectNumberingWithWhitespaces()
```


Allows to specify how numbered list items are recognized when document is imported from plain text format. The default value is  true .

If this option is set to false, lists recognition algorithm detects list paragraphs, when list numbers ends with either dot, right bracket or bullet symbols (such as "\\u2022", "\*", "-" or "o").

If this option is set to true, whitespaces are also used as list number delimiters: list recognition algorithm for Arabic style numbering (1., 1.1.2.) uses both whitespaces and dot (".") symbols.

**Returns:**
boolean - The corresponding  boolean  value.
### setDetectNumberingWithWhitespaces(boolean value) {#setDetectNumberingWithWhitespaces-boolean-}
```
public void setDetectNumberingWithWhitespaces(boolean value)
```


Allows to specify how numbered list items are recognized when document is imported from plain text format. The default value is  true .

If this option is set to false, lists recognition algorithm detects list paragraphs, when list numbers ends with either dot, right bracket or bullet symbols (such as "\\u2022", "\*", "-" or "o").

If this option is set to true, whitespaces are also used as list number delimiters: list recognition algorithm for Arabic style numbering (1., 1.1.2.) uses both whitespaces and dot (".") symbols.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getTrailingSpacesOptions() {#getTrailingSpacesOptions--}
```
public int getTrailingSpacesOptions()
```


Gets preferred option of a trailing space handling. Default value is [TxtTrailingSpacesOptions.TRIM](../../com.aspose.words/txttrailingspacesoptions\#TRIM).

**Returns:**
int - Preferred option of a trailing space handling. The returned value is one of [TxtTrailingSpacesOptions](../../com.aspose.words/txttrailingspacesoptions) constants.
### setTrailingSpacesOptions(int value) {#setTrailingSpacesOptions-int-}
```
public void setTrailingSpacesOptions(int value)
```


Sets preferred option of a trailing space handling. Default value is [TxtTrailingSpacesOptions.TRIM](../../com.aspose.words/txttrailingspacesoptions\#TRIM).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Preferred option of a trailing space handling. The value must be one of [TxtTrailingSpacesOptions](../../com.aspose.words/txttrailingspacesoptions) constants. |

### getLeadingSpacesOptions() {#getLeadingSpacesOptions--}
```
public int getLeadingSpacesOptions()
```


Gets preferred option of a leading space handling. Default value is [TxtLeadingSpacesOptions.CONVERT\_TO\_INDENT](../../com.aspose.words/txtleadingspacesoptions\#CONVERT-TO-INDENT).

**Returns:**
int - Preferred option of a leading space handling. The returned value is one of [TxtLeadingSpacesOptions](../../com.aspose.words/txtleadingspacesoptions) constants.
### setLeadingSpacesOptions(int value) {#setLeadingSpacesOptions-int-}
```
public void setLeadingSpacesOptions(int value)
```


Sets preferred option of a leading space handling. Default value is [TxtLeadingSpacesOptions.CONVERT\_TO\_INDENT](../../com.aspose.words/txtleadingspacesoptions\#CONVERT-TO-INDENT).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Preferred option of a leading space handling. The value must be one of [TxtLeadingSpacesOptions](../../com.aspose.words/txtleadingspacesoptions) constants. |

### getDocumentDirection() {#getDocumentDirection--}
```
public int getDocumentDirection()
```


Gets a document direction. The default value is [DocumentDirection.LEFT\_TO\_RIGHT](../../com.aspose.words/documentdirection\#LEFT-TO-RIGHT).

**Returns:**
int - A document direction. The returned value is one of [DocumentDirection](../../com.aspose.words/documentdirection) constants.
### setDocumentDirection(int value) {#setDocumentDirection-int-}
```
public void setDocumentDirection(int value)
```


Sets a document direction. The default value is [DocumentDirection.LEFT\_TO\_RIGHT](../../com.aspose.words/documentdirection\#LEFT-TO-RIGHT).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A document direction. The value must be one of [DocumentDirection](../../com.aspose.words/documentdirection) constants. |

