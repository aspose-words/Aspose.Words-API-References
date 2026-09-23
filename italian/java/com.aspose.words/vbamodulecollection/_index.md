---
title: "VbaModuleCollection"
linktitle: "VbaModuleCollection"
second_title: "Aspose.Words per Java"
description: "Rappresenta una raccolta di oggetti VbaModule in Java."
type: docs
weight: 707
url: /it/java/com.aspose.words/vbamodulecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class VbaModuleCollection implements Iterable
```

Rappresenta una raccolta di oggetti [VbaModule](../../com.aspose.words/vbamodule/).

Per saperne di più, visita il [ Working with VBA Macros ][Working with VBA Macros] articolo della documentazione.

 **Examples:** 

Mostra come accedere alle informazioni del progetto VBA di un documento.

```

 Document doc = new Document(getMyDir() + "VBA project.docm");

 // A VBA project contains a collection of VBA modules.
 VbaProject vbaProject = doc.getVbaProject();
 System.out.println(vbaProject.isSigned()
         ? MessageFormat.format("Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject.getName(), vbaProject.getCodePage(), vbaProject.getModules().getCount())
         : MessageFormat.format("Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject.getName(), vbaProject.getCodePage(), vbaProject.getModules().getCount()));

 VbaModuleCollection vbaModules = doc.getVbaProject().getModules();

 Assert.assertEquals(vbaModules.getCount(), 3);

 for (VbaModule module : vbaModules) {
     System.out.println(MessageFormat.format("Module name: {0};\nModule code:\n{1}\n", module.getName(), module.getSourceCode()));
 }

 // Set new source code for VBA module. You can access VBA modules in the collection either by index or by name.
 vbaModules.get(0).setSourceCode("Your VBA code...");
 vbaModules.get("Module1").setSourceCode("Your VBA code...");

 // Remove a module from the collection.
 vbaModules.remove(vbaModules.get(2));
 
```


[Working with VBA Macros]: https://docs.aspose.com/words/java/working-with-vba-macros/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [add(VbaModule vbaModule)](#add-com.aspose.words.VbaModule) | Aggiunge un modulo alla raccolta. |
| [get(int index)](#get-int) | Recupera un oggetto [VbaModule](../../com.aspose.words/vbamodule/) per indice. |
| [get(String name)](#get-java.lang.String) | Recupera un oggetto [VbaModule](../../com.aspose.words/vbamodule/) per nome, o Null se non trovato. |
| [getCount()](#getCount) | Restituisce il numero di moduli VBA nella raccolta. |
| [iterator()](#iterator) |  |
| [remove(VbaModule module)](#remove-com.aspose.words.VbaModule) | Rimuove il modulo specificato dalla raccolta. |
### add(VbaModule vbaModule) {#add-com.aspose.words.VbaModule}
```
public void add(VbaModule vbaModule)
```


Aggiunge un modulo alla raccolta.

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

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| vbaModule | [VbaModule](../../com.aspose.words/vbamodule/) |  |

### get(int index) {#get-int}
```
public VbaModule get(int index)
```


Recupera un oggetto [VbaModule](../../com.aspose.words/vbamodule/) per indice.

 **Examples:** 

Mostra come accedere alle informazioni del progetto VBA di un documento.

```

 Document doc = new Document(getMyDir() + "VBA project.docm");

 // A VBA project contains a collection of VBA modules.
 VbaProject vbaProject = doc.getVbaProject();
 System.out.println(vbaProject.isSigned()
         ? MessageFormat.format("Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject.getName(), vbaProject.getCodePage(), vbaProject.getModules().getCount())
         : MessageFormat.format("Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject.getName(), vbaProject.getCodePage(), vbaProject.getModules().getCount()));

 VbaModuleCollection vbaModules = doc.getVbaProject().getModules();

 Assert.assertEquals(vbaModules.getCount(), 3);

 for (VbaModule module : vbaModules) {
     System.out.println(MessageFormat.format("Module name: {0};\nModule code:\n{1}\n", module.getName(), module.getSourceCode()));
 }

 // Set new source code for VBA module. You can access VBA modules in the collection either by index or by name.
 vbaModules.get(0).setSourceCode("Your VBA code...");
 vbaModules.get("Module1").setSourceCode("Your VBA code...");

 // Remove a module from the collection.
 vbaModules.remove(vbaModules.get(2));
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | Indice basato su zero del modulo da recuperare. |

**Returns:**
[VbaModule](../../com.aspose.words/vbamodule/) - The corresponding [VbaModule](../../com.aspose.words/vbamodule/) value.
### get(String name) {#get-java.lang.String}
```
public VbaModule get(String name)
```


Recupera un oggetto [VbaModule](../../com.aspose.words/vbamodule/) per nome, o Null se non trovato.

 **Examples:** 

Mostra come accedere alle informazioni del progetto VBA di un documento.

```

 Document doc = new Document(getMyDir() + "VBA project.docm");

 // A VBA project contains a collection of VBA modules.
 VbaProject vbaProject = doc.getVbaProject();
 System.out.println(vbaProject.isSigned()
         ? MessageFormat.format("Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject.getName(), vbaProject.getCodePage(), vbaProject.getModules().getCount())
         : MessageFormat.format("Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject.getName(), vbaProject.getCodePage(), vbaProject.getModules().getCount()));

 VbaModuleCollection vbaModules = doc.getVbaProject().getModules();

 Assert.assertEquals(vbaModules.getCount(), 3);

 for (VbaModule module : vbaModules) {
     System.out.println(MessageFormat.format("Module name: {0};\nModule code:\n{1}\n", module.getName(), module.getSourceCode()));
 }

 // Set new source code for VBA module. You can access VBA modules in the collection either by index or by name.
 vbaModules.get(0).setSourceCode("Your VBA code...");
 vbaModules.get("Module1").setSourceCode("Your VBA code...");

 // Remove a module from the collection.
 vbaModules.remove(vbaModules.get(2));
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[VbaModule](../../com.aspose.words/vbamodule/) - The corresponding [VbaModule](../../com.aspose.words/vbamodule/) value.
### getCount() {#getCount}
```
public int getCount()
```


Restituisce il numero di moduli VBA nella raccolta.

 **Examples:** 

Mostra come accedere alle informazioni del progetto VBA di un documento.

```

 Document doc = new Document(getMyDir() + "VBA project.docm");

 // A VBA project contains a collection of VBA modules.
 VbaProject vbaProject = doc.getVbaProject();
 System.out.println(vbaProject.isSigned()
         ? MessageFormat.format("Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject.getName(), vbaProject.getCodePage(), vbaProject.getModules().getCount())
         : MessageFormat.format("Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject.getName(), vbaProject.getCodePage(), vbaProject.getModules().getCount()));

 VbaModuleCollection vbaModules = doc.getVbaProject().getModules();

 Assert.assertEquals(vbaModules.getCount(), 3);

 for (VbaModule module : vbaModules) {
     System.out.println(MessageFormat.format("Module name: {0};\nModule code:\n{1}\n", module.getName(), module.getSourceCode()));
 }

 // Set new source code for VBA module. You can access VBA modules in the collection either by index or by name.
 vbaModules.get(0).setSourceCode("Your VBA code...");
 vbaModules.get("Module1").setSourceCode("Your VBA code...");

 // Remove a module from the collection.
 vbaModules.remove(vbaModules.get(2));
 
```

**Returns:**
int - Il numero di moduli VBA nella raccolta.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(VbaModule module) {#remove-com.aspose.words.VbaModule}
```
public void remove(VbaModule module)
```


Rimuove il modulo specificato dalla raccolta.

 **Examples:** 

Mostra come accedere alle informazioni del progetto VBA di un documento.

```

 Document doc = new Document(getMyDir() + "VBA project.docm");

 // A VBA project contains a collection of VBA modules.
 VbaProject vbaProject = doc.getVbaProject();
 System.out.println(vbaProject.isSigned()
         ? MessageFormat.format("Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject.getName(), vbaProject.getCodePage(), vbaProject.getModules().getCount())
         : MessageFormat.format("Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject.getName(), vbaProject.getCodePage(), vbaProject.getModules().getCount()));

 VbaModuleCollection vbaModules = doc.getVbaProject().getModules();

 Assert.assertEquals(vbaModules.getCount(), 3);

 for (VbaModule module : vbaModules) {
     System.out.println(MessageFormat.format("Module name: {0};\nModule code:\n{1}\n", module.getName(), module.getSourceCode()));
 }

 // Set new source code for VBA module. You can access VBA modules in the collection either by index or by name.
 vbaModules.get(0).setSourceCode("Your VBA code...");
 vbaModules.get("Module1").setSourceCode("Your VBA code...");

 // Remove a module from the collection.
 vbaModules.remove(vbaModules.get(2));
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| module | [VbaModule](../../com.aspose.words/vbamodule/) | Il modulo da rimuovere. |

