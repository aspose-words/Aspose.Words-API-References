---
title: VbaModuleType
second_title: Aspose.Words for Java API Reference
description: Specifies the type of a model in a VBA project.
type: docs
weight: 595
url: /java/com.aspose.words/vbamoduletype/
---

**Inheritance:**
java.lang.Object
```
public class VbaModuleType
```

Specifies the type of a model in a VBA project.
## Fields

| Field | Description |
| --- | --- |
| [DOCUMENT_MODULE](#DOCUMENT-MODULE) | A type of VBA project item that specifies a module for embedded macros and programmatic access operations that are associated with a document. |
| [PROCEDURAL_MODULE](#PROCEDURAL-MODULE) | A collection of subroutines and functions. |
| [CLASS_MODULE](#CLASS-MODULE) | A module that contains the definition for a new object. |
| [DESIGNER_MODULE](#DESIGNER-MODULE) | A VBA module that extends the methods and properties of an ActiveX control that has been registered with the project. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int vbaModuleType)](#getName-int-) |  |
| [toString(int vbaModuleType)](#toString-int-) |  |
| [fromName(String vbaModuleTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### DOCUMENT_MODULE {#DOCUMENT-MODULE}
```
public static int DOCUMENT_MODULE
```


A type of VBA project item that specifies a module for embedded macros and programmatic access operations that are associated with a document.

### PROCEDURAL_MODULE {#PROCEDURAL-MODULE}
```
public static int PROCEDURAL_MODULE
```


A collection of subroutines and functions.

### CLASS_MODULE {#CLASS-MODULE}
```
public static int CLASS_MODULE
```


A module that contains the definition for a new object. Each instance of a class creates a new object, and procedures that are defined in the module become properties and methods of the object.

### DESIGNER_MODULE {#DESIGNER-MODULE}
```
public static int DESIGNER_MODULE
```


A VBA module that extends the methods and properties of an ActiveX control that has been registered with the project.

### length {#length}
```
public static int length
```


### getName(int vbaModuleType) {#getName-int-}
```
public static String getName(int vbaModuleType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| vbaModuleType | int |  |

**Returns:**
java.lang.String
### toString(int vbaModuleType) {#toString-int-}
```
public static String toString(int vbaModuleType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| vbaModuleType | int |  |

**Returns:**
java.lang.String
### fromName(String vbaModuleTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String vbaModuleTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| vbaModuleTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
