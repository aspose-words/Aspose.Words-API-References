---
title: VbaProject
second_title: Aspose.Words for Java API Reference
description: Provides access to VBA project information.
type: docs
weight: 596
url: /java/com.aspose.words/vbaproject/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class VbaProject implements Cloneable
```

Provides access to VBA project information. A VBA project inside the document is defined as a collection of VBA modules.

To learn more, visit the **Working with VBA Macros** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [VbaProject()](#VbaProject--) | Creates a blank VbaProject. |
## Methods

| Method | Description |
| --- | --- |
| [getName()](#getName--) | Gets VBA project name. |
| [setName(String value)](#setName-java.lang.String-) | Sets VBA project name. |
| [getModules()](#getModules--) | Returns collection of VBA project modules. |
| [getCodePage()](#getCodePage--) | Returns the VBA project\\u2019s code page. |
| [deepClone()](#deepClone--) | Performs a copy of the [VbaProject](../../com.aspose.words/vbaproject). |
| [isSigned()](#isSigned--) | Shows whether the VbaProject is signed or not. |
| [getReferences()](#getReferences--) | Gets a collection of VBA project references. |
### VbaProject() {#VbaProject--}
```
public VbaProject()
```


Creates a blank VbaProject.

### getName() {#getName--}
```
public String getName()
```


Gets VBA project name.

**Returns:**
java.lang.String - VBA project name.
### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Sets VBA project name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | VBA project name. |

### getModules() {#getModules--}
```
public VbaModuleCollection getModules()
```


Returns collection of VBA project modules.

**Returns:**
[VbaModuleCollection](../../com.aspose.words/vbamodulecollection) - Collection of VBA project modules.
### getCodePage() {#getCodePage--}
```
public int getCodePage()
```


Returns the VBA project\\u2019s code page.

**Returns:**
int - The VBA project\\u2019s code page.
### deepClone() {#deepClone--}
```
public VbaProject deepClone()
```


Performs a copy of the [VbaProject](../../com.aspose.words/vbaproject).

**Returns:**
[VbaProject](../../com.aspose.words/vbaproject) - The cloned VbaProject.
### isSigned() {#isSigned--}
```
public boolean isSigned()
```


Shows whether the VbaProject is signed or not.

**Returns:**
boolean - The corresponding  boolean  value.
### getReferences() {#getReferences--}
```
public VbaReferenceCollection getReferences()
```


Gets a collection of VBA project references.

**Returns:**
[VbaReferenceCollection](../../com.aspose.words/vbareferencecollection) - A collection of VBA project references.
