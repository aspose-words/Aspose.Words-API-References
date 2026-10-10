---
title: "VbaModuleType"
linktitle: "VbaModuleType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type d'un modèle dans un projet VBA en Java."
type: docs
weight: 708
url: /fr/java/com.aspose.words/vbamoduletype/
---

**Inheritance:**
java.lang.Object
```
public class VbaModuleType
```

Spécifie le type d'un modèle dans un projet VBA.

 **Examples:** 

Montre comment créer un projet VBA en utilisant des macros.

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
## Champs

| Champ | Description |
| --- | --- |
| [CLASS_MODULE](#CLASS-MODULE) | Un module qui contient la définition d'un nouvel objet. |
| [DESIGNER_MODULE](#DESIGNER-MODULE) | Un module VBA qui étend les méthodes et propriétés d'un contrôle ActiveX qui a été enregistré dans le projet. |
| [DOCUMENT_MODULE](#DOCUMENT-MODULE) | Un type d'élément de projet VBA qui spécifie un module pour les macros intégrées et les opérations d'accès programmatique associées à un document. |
| [PROCEDURAL_MODULE](#PROCEDURAL-MODULE) | Une collection de sous‑routines et de fonctions. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String vbaModuleTypeName)](#fromName-java.lang.String) |  |
| [getName(int vbaModuleType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int vbaModuleType)](#toString-int) |  |
### CLASS_MODULE {#CLASS-MODULE}
```
public static int CLASS_MODULE
```


Un module qui contient la définition d'un nouvel objet. Chaque instance d'une classe crée un nouvel objet, et les procédures définies dans le module deviennent des propriétés et des méthodes de l'objet.

### DESIGNER_MODULE {#DESIGNER-MODULE}
```
public static int DESIGNER_MODULE
```


Un module VBA qui étend les méthodes et propriétés d'un contrôle ActiveX qui a été enregistré dans le projet.

### DOCUMENT_MODULE {#DOCUMENT-MODULE}
```
public static int DOCUMENT_MODULE
```


Un type d'élément de projet VBA qui spécifie un module pour les macros intégrées et les opérations d'accès programmatique associées à un document.

### PROCEDURAL_MODULE {#PROCEDURAL-MODULE}
```
public static int PROCEDURAL_MODULE
```


Une collection de sous‑routines et de fonctions.

### length {#length}
```
public static int length
```


### fromName(String vbaModuleTypeName) {#fromName-java.lang.String}
```
public static int fromName(String vbaModuleTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| vbaModuleTypeName | java.lang.String |  |

**Returns:**
int
### getName(int vbaModuleType) {#getName-int}
```
public static String getName(int vbaModuleType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| vbaModuleType | int |  |

**Returns:**
java.lang.String
