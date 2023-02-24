---
title: BuildingBlockType
linktitle: BuildingBlockType
second_title: Aspose.Words for Java API Reference
description: Specifies a building block type in Java.
type: docs
weight: 45
url: /java/com.aspose.words/buildingblocktype/
---

**Inheritance:**
java.lang.Object
```
public class BuildingBlockType
```

Specifies a building block type. The type might affect the visibility and behavior of the building block in Microsoft Word.

Corresponds to the **ST\_DocPartType** type in OOXML.
## Fields

| Field | Description |
| --- | --- |
| [ALL](#ALL) | The building block is associated with all types. |
| [AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT](#AUTOMATICALLY-REPLACE-NAME-WITH-CONTENT) | Allows the building block to be automatically inserted into the document whenever its name is entered into an application. |
| [AUTO_CORRECT](#AUTO-CORRECT) | The building block is associated with the spelling and grammar tools. |
| [AUTO_TEXT](#AUTO-TEXT) | The building block is an AutoText entry. |
| [DEFAULT](#DEFAULT) | Save as [NONE](../../com.aspose.words/buildingblocktype/\#NONE). |
| [FORM_FIELD_HELP_TEXT](#FORM-FIELD-HELP-TEXT) | The building block is a form field help text. |
| [NONE](#NONE) | No type information is specified for the building block. |
| [NORMAL](#NORMAL) | The building block is a normal (i.e. |
| [STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT](#STRUCTURED-DOCUMENT-TAG-PLACEHOLDER-TEXT) | The building block is a structured document tag placeholder text. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String buildingBlockTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int buildingBlockType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int buildingBlockType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### ALL {#ALL}
```
public static int ALL
```


The building block is associated with all types.

### AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT {#AUTOMATICALLY-REPLACE-NAME-WITH-CONTENT}
```
public static int AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT
```


Allows the building block to be automatically inserted into the document whenever its name is entered into an application.

### AUTO_CORRECT {#AUTO-CORRECT}
```
public static int AUTO_CORRECT
```


The building block is associated with the spelling and grammar tools.

### AUTO_TEXT {#AUTO-TEXT}
```
public static int AUTO_TEXT
```


The building block is an AutoText entry.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Save as [NONE](../../com.aspose.words/buildingblocktype/\#NONE).

### FORM_FIELD_HELP_TEXT {#FORM-FIELD-HELP-TEXT}
```
public static int FORM_FIELD_HELP_TEXT
```


The building block is a form field help text.

### NONE {#NONE}
```
public static int NONE
```


No type information is specified for the building block.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


The building block is a normal (i.e. regular) glossary document entry.

### STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT {#STRUCTURED-DOCUMENT-TAG-PLACEHOLDER-TEXT}
```
public static int STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT
```


The building block is a structured document tag placeholder text.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fromName(String buildingBlockTypeName) {#fromName-java.lang.String}
```
public static int fromName(String buildingBlockTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| buildingBlockTypeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int buildingBlockType) {#getName-int}
```
public static String getName(int buildingBlockType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| buildingBlockType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(int buildingBlockType) {#toString-int}
```
public static String toString(int buildingBlockType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| buildingBlockType | int |  |

**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

