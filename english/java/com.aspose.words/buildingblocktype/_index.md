---
title: BuildingBlockType
second_title: Aspose.Words for Java API Reference
description: Specifies a building block type.
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
| [NONE](#NONE) | No type information is specified for the building block. |
| [AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT](#AUTOMATICALLY-REPLACE-NAME-WITH-CONTENT) | Allows the building block to be automatically inserted into the document whenever its name is entered into an application. |
| [STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT](#STRUCTURED-DOCUMENT-TAG-PLACEHOLDER-TEXT) | The building block is a structured document tag placeholder text. |
| [FORM_FIELD_HELP_TEXT](#FORM-FIELD-HELP-TEXT) | The building block is a form field help text. |
| [NORMAL](#NORMAL) | The building block is a normal (i.e. |
| [AUTO_CORRECT](#AUTO-CORRECT) | The building block is associated with the spelling and grammar tools. |
| [AUTO_TEXT](#AUTO-TEXT) | The building block is an AutoText entry. |
| [ALL](#ALL) | The building block is associated with all types. |
| [DEFAULT](#DEFAULT) | Save as [NONE](../../com.aspose.words/buildingblocktype\#NONE). |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int buildingBlockType)](#getName-int-) |  |
| [toString(int buildingBlockType)](#toString-int-) |  |
| [fromName(String buildingBlockTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### NONE {#NONE}
```
public static int NONE
```


No type information is specified for the building block.

### AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT {#AUTOMATICALLY-REPLACE-NAME-WITH-CONTENT}
```
public static int AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT
```


Allows the building block to be automatically inserted into the document whenever its name is entered into an application.

### STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT {#STRUCTURED-DOCUMENT-TAG-PLACEHOLDER-TEXT}
```
public static int STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT
```


The building block is a structured document tag placeholder text.

### FORM_FIELD_HELP_TEXT {#FORM-FIELD-HELP-TEXT}
```
public static int FORM_FIELD_HELP_TEXT
```


The building block is a form field help text.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


The building block is a normal (i.e. regular) glossary document entry.

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

### ALL {#ALL}
```
public static int ALL
```


The building block is associated with all types.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Save as [NONE](../../com.aspose.words/buildingblocktype\#NONE).

### length {#length}
```
public static int length
```


### getName(int buildingBlockType) {#getName-int-}
```
public static String getName(int buildingBlockType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| buildingBlockType | int |  |

**Returns:**
java.lang.String
### toString(int buildingBlockType) {#toString-int-}
```
public static String toString(int buildingBlockType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| buildingBlockType | int |  |

**Returns:**
java.lang.String
### fromName(String buildingBlockTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String buildingBlockTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| buildingBlockTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
