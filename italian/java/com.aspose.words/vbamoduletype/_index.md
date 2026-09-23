---
title: "VbaModuleType"
linktitle: "VbaModuleType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di modello in un progetto VBA in Java."
type: docs
weight: 708
url: /it/java/com.aspose.words/vbamoduletype/
---

**Inheritance:**
java.lang.Object
```
public class VbaModuleType
```

Specifica il tipo di modello in un progetto VBA.

 **Examples:** 

Mostra come creare un progetto VBA usando le macro.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [CLASS_MODULE](#CLASS-MODULE) | Un modulo che contiene la definizione di un nuovo oggetto. |
| [DESIGNER_MODULE](#DESIGNER-MODULE) | Un modulo VBA che estende i metodi e le proprietà di un controllo ActiveX registrato nel progetto. |
| [DOCUMENT_MODULE](#DOCUMENT-MODULE) | Un tipo di elemento del progetto VBA che specifica un modulo per macro incorporate e operazioni di accesso programmatico associate a un documento. |
| [PROCEDURAL_MODULE](#PROCEDURAL-MODULE) | Una raccolta di subroutine e funzioni. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String vbaModuleTypeName)](#fromName-java.lang.String) |  |
| [getName(int vbaModuleType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int vbaModuleType)](#toString-int) |  |
### CLASS_MODULE {#CLASS-MODULE}
```
public static int CLASS_MODULE
```


Un modulo che contiene la definizione di un nuovo oggetto. Ogni istanza di una classe crea un nuovo oggetto e le procedure definite nel modulo diventano proprietà e metodi dell'oggetto.

### DESIGNER_MODULE {#DESIGNER-MODULE}
```
public static int DESIGNER_MODULE
```


Un modulo VBA che estende i metodi e le proprietà di un controllo ActiveX registrato nel progetto.

### DOCUMENT_MODULE {#DOCUMENT-MODULE}
```
public static int DOCUMENT_MODULE
```


Un tipo di elemento del progetto VBA che specifica un modulo per macro incorporate e operazioni di accesso programmatico associate a un documento.

### PROCEDURAL_MODULE {#PROCEDURAL-MODULE}
```
public static int PROCEDURAL_MODULE
```


Una raccolta di subroutine e funzioni.

### length {#length}
```
public static int length
```


### fromName(String vbaModuleTypeName) {#fromName-java.lang.String}
```
public static int fromName(String vbaModuleTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| vbaModuleTypeName | java.lang.String |  |

**Returns:**
int
### getName(int vbaModuleType) {#getName-int}
```
public static String getName(int vbaModuleType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| vbaModuleType | int |  |

**Returns:**
java.lang.String
