---
title: "VbaModuleType"
linktitle: "VbaModuleType"
second_title: "Aspose.Words для Java"
description: "Указывает тип модели в проекте VBA на Java."
type: docs
weight: 708
url: /ru/java/com.aspose.words/vbamoduletype/
---

**Inheritance:**
java.lang.Object
```
public class VbaModuleType
```

Указывает тип модели в проекте VBA.

 **Examples:** 

Показывает, как создать проект VBA с использованием макросов.

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
## Поля

| Поле | Описание |
| --- | --- |
| [CLASS_MODULE](#CLASS-MODULE) | Модуль, содержащий определение нового объекта. |
| [DESIGNER_MODULE](#DESIGNER-MODULE) | Модуль VBA, который расширяет методы и свойства ActiveX‑контрола, зарегистрированного в проекте. |
| [DOCUMENT_MODULE](#DOCUMENT-MODULE) | Тип элемента проекта VBA, указывающий модуль для встроенных макросов и операций программного доступа, связанных с документом. |
| [PROCEDURAL_MODULE](#PROCEDURAL-MODULE) | Коллекция подпрограмм и функций. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String vbaModuleTypeName)](#fromName-java.lang.String) |  |
| [getName(int vbaModuleType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int vbaModuleType)](#toString-int) |  |
### CLASS_MODULE {#CLASS-MODULE}
```
public static int CLASS_MODULE
```


Модуль, содержащий определение нового объекта. Каждый экземпляр класса создает новый объект, а процедуры, определённые в модуле, становятся свойствами и методами объекта.

### DESIGNER_MODULE {#DESIGNER-MODULE}
```
public static int DESIGNER_MODULE
```


Модуль VBA, который расширяет методы и свойства ActiveX‑контрола, зарегистрированного в проекте.

### DOCUMENT_MODULE {#DOCUMENT-MODULE}
```
public static int DOCUMENT_MODULE
```


Тип элемента проекта VBA, указывающий модуль для встроенных макросов и операций программного доступа, связанных с документом.

### PROCEDURAL_MODULE {#PROCEDURAL-MODULE}
```
public static int PROCEDURAL_MODULE
```


Коллекция подпрограмм и функций.

### length {#length}
```
public static int length
```


### fromName(String vbaModuleTypeName) {#fromName-java.lang.String}
```
public static int fromName(String vbaModuleTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| vbaModuleTypeName | java.lang.String |  |

**Returns:**
int
### getName(int vbaModuleType) {#getName-int}
```
public static String getName(int vbaModuleType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| vbaModuleType | int |  |

**Returns:**
java.lang.String
