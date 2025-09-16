---
title: DocumentRecoveryMode
linktitle: DocumentRecoveryMode
second_title: Aspose.Words for Java
description: Specifies the available recovery options when a document encounters errors during loading in Java.
type: docs
weight: 170
url: /java/com.aspose.words/documentrecoverymode/
---

**Inheritance:**
java.lang.Object
```
public class DocumentRecoveryMode
```

Specifies the available recovery options when a document encounters errors during loading.

 **Examples:** 

Shows how to try to recover a document if errors occurred during loading.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | No recovery is attempted. |
| [TRY_RECOVER](#TRY-RECOVER) | Attempts to recover the document while preserving as much data as possible. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String documentRecoveryModeName)](#fromName-java.lang.String) |  |
| [getName(int documentRecoveryMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentRecoveryMode)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


No recovery is attempted. If the document is invalid, loading will fail with an error.

### TRY_RECOVER {#TRY-RECOVER}
```
public static int TRY_RECOVER
```


Attempts to recover the document while preserving as much data as possible.

### length {#length}
```
public static int length
```


### fromName(String documentRecoveryModeName) {#fromName-java.lang.String}
```
public static int fromName(String documentRecoveryModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentRecoveryModeName | java.lang.String |  |

**Returns:**
int
### getName(int documentRecoveryMode) {#getName-int}
```
public static String getName(int documentRecoveryMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int documentRecoveryMode) {#toString-int}
```
public static String toString(int documentRecoveryMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
