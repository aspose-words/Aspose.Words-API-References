---
title: "VbaModuleType"
linktitle: "VbaModuleType"
second_title: "Aspose.Words für Java"
description: "Gibt den Typ eines Modells in einem VBA-Projekt in Java an."
type: docs
weight: 708
url: /de/java/com.aspose.words/vbamoduletype/
---

**Inheritance:**
java.lang.Object
```
public class VbaModuleType
```

Gibt den Typ eines Modells in einem VBA-Projekt an.

 **Examples:** 

Zeigt, wie man ein VBA-Projekt mit Makros erstellt.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CLASS_MODULE](#CLASS-MODULE) | Ein Modul, das die Definition für ein neues Objekt enthält. |
| [DESIGNER_MODULE](#DESIGNER-MODULE) | Ein VBA-Modul, das die Methoden und Eigenschaften eines ActiveX-Steuerelements erweitert, das im Projekt registriert wurde. |
| [DOCUMENT_MODULE](#DOCUMENT-MODULE) | Ein Typ von VBA-Projekt-Element, das ein Modul für eingebettete Makros und programmgesteuerte Zugriffsoperationen angibt, die mit einem Dokument verknüpft sind. |
| [PROCEDURAL_MODULE](#PROCEDURAL-MODULE) | Eine Sammlung von Subroutinen und Funktionen. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String vbaModuleTypeName)](#fromName-java.lang.String) |  |
| [getName(int vbaModuleType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int vbaModuleType)](#toString-int) |  |
### CLASS_MODULE {#CLASS-MODULE}
```
public static int CLASS_MODULE
```


Ein Modul, das die Definition für ein neues Objekt enthält. Jede Instanz einer Klasse erzeugt ein neues Objekt, und im Modul definierte Prozeduren werden zu Eigenschaften und Methoden des Objekts.

### DESIGNER_MODULE {#DESIGNER-MODULE}
```
public static int DESIGNER_MODULE
```


Ein VBA-Modul, das die Methoden und Eigenschaften eines ActiveX-Steuerelements erweitert, das im Projekt registriert wurde.

### DOCUMENT_MODULE {#DOCUMENT-MODULE}
```
public static int DOCUMENT_MODULE
```


Ein Typ von VBA-Projekt-Element, das ein Modul für eingebettete Makros und programmgesteuerte Zugriffsoperationen angibt, die mit einem Dokument verknüpft sind.

### PROCEDURAL_MODULE {#PROCEDURAL-MODULE}
```
public static int PROCEDURAL_MODULE
```


Eine Sammlung von Subroutinen und Funktionen.

### length {#length}
```
public static int length
```


### fromName(String vbaModuleTypeName) {#fromName-java.lang.String}
```
public static int fromName(String vbaModuleTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| vbaModuleTypeName | java.lang.String |  |

**Returns:**
int
### getName(int vbaModuleType) {#getName-int}
```
public static String getName(int vbaModuleType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| vbaModuleType | int |  |

**Returns:**
java.lang.String
