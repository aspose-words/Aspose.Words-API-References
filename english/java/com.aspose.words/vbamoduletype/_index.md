---
title: VbaModuleType
linktitle: VbaModuleType
second_title: Aspose.Words for Java
description: Specifies the type of a model in a VBA project in Java.
type: docs
weight: 657
url: /java/com.aspose.words/vbamoduletype/
---

**Inheritance:**
java.lang.Object
```
public class VbaModuleType
```

Specifies the type of a model in a VBA project.

 **Examples:** 

Shows how to create a VBA project using macros.

```

 Document doc = new Document();

 // Create a new VBA project.
 VbaProject project = new VbaProject();
 project.setName("Aspose.Project");
 doc.setVbaProject(project);

 // Create a new module and specify a macro source code.
 VbaModule module = new VbaModule();
 module.setName("Aspose.Module");
 module.setType(VbaModuleType.PROCEDURAL_MODULE);
 module.setSourceCode("New source code");

 // Add the module to the VBA project.
 doc.getVbaProject().getModules().add(module);

 doc.save(getArtifactsDir() + "VbaProject.CreateVBAMacros.docm");
 
```
## Fields

| Field | Description |
| --- | --- |
| [CLASS_MODULE](#CLASS-MODULE) | A module that contains the definition for a new object. |
| [DESIGNER_MODULE](#DESIGNER-MODULE) | A VBA module that extends the methods and properties of an ActiveX control that has been registered with the project. |
| [DOCUMENT_MODULE](#DOCUMENT-MODULE) | A type of VBA project item that specifies a module for embedded macros and programmatic access operations that are associated with a document. |
| [PROCEDURAL_MODULE](#PROCEDURAL-MODULE) | A collection of subroutines and functions. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String vbaModuleTypeName)](#fromName-java.lang.String) |  |
| [getName(int vbaModuleType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int vbaModuleType)](#toString-int) |  |
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

### length {#length}
```
public static int length
```


### fromName(String vbaModuleTypeName) {#fromName-java.lang.String}
```
public static int fromName(String vbaModuleTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| vbaModuleTypeName | java.lang.String |  |

**Returns:**
int
### getName(int vbaModuleType) {#getName-int}
```
public static String getName(int vbaModuleType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| vbaModuleType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int vbaModuleType) {#toString-int}
```
public static String toString(int vbaModuleType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| vbaModuleType | int |  |

**Returns:**
java.lang.String
