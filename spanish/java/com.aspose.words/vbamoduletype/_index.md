---
title: "VbaModuleType"
linktitle: "VbaModuleType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de un modelo en un proyecto VBA en Java."
type: docs
weight: 708
url: /es/java/com.aspose.words/vbamoduletype/
---

**Inheritance:**
java.lang.Object
```
public class VbaModuleType
```

Especifica el tipo de modelo en un proyecto VBA.

 **Examples:** 

Muestra cómo crear un proyecto VBA usando macros.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [CLASS_MODULE](#CLASS-MODULE) | Un módulo que contiene la definición de un nuevo objeto. |
| [DESIGNER_MODULE](#DESIGNER-MODULE) | Un módulo VBA que amplía los métodos y propiedades de un control ActiveX que ha sido registrado en el proyecto. |
| [DOCUMENT_MODULE](#DOCUMENT-MODULE) | Un tipo de elemento de proyecto VBA que especifica un módulo para macros incrustados y operaciones de acceso programático asociadas a un documento. |
| [PROCEDURAL_MODULE](#PROCEDURAL-MODULE) | Una colección de subrutinas y funciones. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String vbaModuleTypeName)](#fromName-java.lang.String) |  |
| [getName(int vbaModuleType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int vbaModuleType)](#toString-int) |  |
### CLASS_MODULE {#CLASS-MODULE}
```
public static int CLASS_MODULE
```


Un módulo que contiene la definición de un nuevo objeto. Cada instancia de una clase crea un nuevo objeto, y los procedimientos definidos en el módulo se convierten en propiedades y métodos del objeto.

### DESIGNER_MODULE {#DESIGNER-MODULE}
```
public static int DESIGNER_MODULE
```


Un módulo VBA que amplía los métodos y propiedades de un control ActiveX que ha sido registrado en el proyecto.

### DOCUMENT_MODULE {#DOCUMENT-MODULE}
```
public static int DOCUMENT_MODULE
```


Un tipo de elemento de proyecto VBA que especifica un módulo para macros incrustados y operaciones de acceso programático asociadas a un documento.

### PROCEDURAL_MODULE {#PROCEDURAL-MODULE}
```
public static int PROCEDURAL_MODULE
```


Una colección de subrutinas y funciones.

### length {#length}
```
public static int length
```


### fromName(String vbaModuleTypeName) {#fromName-java.lang.String}
```
public static int fromName(String vbaModuleTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| vbaModuleTypeName | java.lang.String |  |

**Returns:**
int
### getName(int vbaModuleType) {#getName-int}
```
public static String getName(int vbaModuleType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| vbaModuleType | int |  |

**Returns:**
java.lang.String
