---
title: ProtectionType
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 470
url: /java/com.aspose.words/protectiontype/
---

**Inheritance:**
java.lang.Object
```
public class ProtectionType
```

A utility class providing constants. Protection type for a document.
## Fields

| Field | Description |
| --- | --- |
| [ALLOW_ONLY_COMMENTS](#ALLOW-ONLY-COMMENTS) | User can only modify comments in the document. |
| [ALLOW_ONLY_FORM_FIELDS](#ALLOW-ONLY-FORM-FIELDS) | User can only enter data in the form fields in the document. |
| [ALLOW_ONLY_REVISIONS](#ALLOW-ONLY-REVISIONS) | User can only add revision marks to the document. |
| [READ_ONLY](#READ-ONLY) | No changes are allowed to the document. |
| [NO_PROTECTION](#NO-PROTECTION) | The document is not protected. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int protectionType)](#getName-int-) |  |
| [toString(int protectionType)](#toString-int-) |  |
| [fromName(String protectionTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### ALLOW_ONLY_COMMENTS {#ALLOW-ONLY-COMMENTS}
```
public static int ALLOW_ONLY_COMMENTS
```


User can only modify comments in the document.

### ALLOW_ONLY_FORM_FIELDS {#ALLOW-ONLY-FORM-FIELDS}
```
public static int ALLOW_ONLY_FORM_FIELDS
```


User can only enter data in the form fields in the document.

### ALLOW_ONLY_REVISIONS {#ALLOW-ONLY-REVISIONS}
```
public static int ALLOW_ONLY_REVISIONS
```


User can only add revision marks to the document.

### READ_ONLY {#READ-ONLY}
```
public static int READ_ONLY
```


No changes are allowed to the document. Available since Microsoft Word 2003.

### NO_PROTECTION {#NO-PROTECTION}
```
public static int NO_PROTECTION
```


The document is not protected.

### length {#length}
```
public static int length
```


### getName(int protectionType) {#getName-int-}
```
public static String getName(int protectionType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| protectionType | int |  |

**Returns:**
java.lang.String
### toString(int protectionType) {#toString-int-}
```
public static String toString(int protectionType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| protectionType | int |  |

**Returns:**
java.lang.String
### fromName(String protectionTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String protectionTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| protectionTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
