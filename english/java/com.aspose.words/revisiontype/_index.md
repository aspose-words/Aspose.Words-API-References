---
title: RevisionType
second_title: Aspose.Words for Java API Reference
description: Specifies the type of change being tracked in .
type: docs
weight: 490
url: /java/com.aspose.words/revisiontype/
---

**Inheritance:**
java.lang.Object
```
public class RevisionType
```

Specifies the type of change being tracked in [Revision](../../com.aspose.words/revision).
## Fields

| Field | Description |
| --- | --- |
| [INSERTION](#INSERTION) | New content was inserted in the document. |
| [DELETION](#DELETION) | Content was removed from the document. |
| [FORMAT_CHANGE](#FORMAT-CHANGE) | Change of formatting was applied to the parent node. |
| [STYLE_DEFINITION_CHANGE](#STYLE-DEFINITION-CHANGE) | Change of formatting was applied to the parent style. |
| [MOVING](#MOVING) | Content was moved in the document. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int revisionType)](#getName-int-) |  |
| [toString(int revisionType)](#toString-int-) |  |
| [fromName(String revisionTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### INSERTION {#INSERTION}
```
public static int INSERTION
```


New content was inserted in the document.

### DELETION {#DELETION}
```
public static int DELETION
```


Content was removed from the document.

### FORMAT_CHANGE {#FORMAT-CHANGE}
```
public static int FORMAT_CHANGE
```


Change of formatting was applied to the parent node.

### STYLE_DEFINITION_CHANGE {#STYLE-DEFINITION-CHANGE}
```
public static int STYLE_DEFINITION_CHANGE
```


Change of formatting was applied to the parent style.

### MOVING {#MOVING}
```
public static int MOVING
```


Content was moved in the document.

### length {#length}
```
public static int length
```


### getName(int revisionType) {#getName-int-}
```
public static String getName(int revisionType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionType | int |  |

**Returns:**
java.lang.String
### toString(int revisionType) {#toString-int-}
```
public static String toString(int revisionType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionType | int |  |

**Returns:**
java.lang.String
### fromName(String revisionTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String revisionTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
