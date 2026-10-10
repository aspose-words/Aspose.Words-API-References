---
title: "VbaModuleCollection"
linktitle: "VbaModuleCollection"
second_title: "Aspose.Words für Java"
description: "Stellt eine Sammlung von VbaModule‑Objekten in Java dar."
type: docs
weight: 707
url: /de/java/com.aspose.words/vbamodulecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class VbaModuleCollection implements Iterable
```

Stellt eine Sammlung von [VbaModule](../../com.aspose.words/vbamodule/) Objekten dar.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with VBA Macros ][Working with VBA Macros].

 **Examples:** 

Zeigt, wie man auf die VBA-Projektinformationen eines Dokuments zugreift.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(VbaModule vbaModule)](#add-com.aspose.words.VbaModule) | Fügt der Sammlung ein Modul hinzu. |
| [get(int index)](#get-int) | Ruft ein [VbaModule](../../com.aspose.words/vbamodule/) Objekt anhand des Index ab. |
| [get(String name)](#get-java.lang.String) | Ruft ein [VbaModule](../../com.aspose.words/vbamodule/) Objekt anhand des Namens ab, oder Null, wenn nicht gefunden. |
| [getCount()](#getCount) | Gibt die Anzahl der VBA‑Module in der Sammlung zurück. |
| [iterator()](#iterator) |  |
| [remove(VbaModule module)](#remove-com.aspose.words.VbaModule) | Entfernt das angegebene Modul aus der Sammlung. |
### add(VbaModule vbaModule) {#add-com.aspose.words.VbaModule}
```
public void add(VbaModule vbaModule)
```


Fügt der Sammlung ein Modul hinzu.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| vbaModule | [VbaModule](../../com.aspose.words/vbamodule/) |  |

### get(int index) {#get-int}
```
public VbaModule get(int index)
```


Ruft ein [VbaModule](../../com.aspose.words/vbamodule/) Objekt anhand des Index ab.

 **Examples:** 

Zeigt, wie man auf die VBA-Projektinformationen eines Dokuments zugreift.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Nullbasierter Index des abzurufenden Moduls. |

**Returns:**
[VbaModule](../../com.aspose.words/vbamodule/) - The corresponding [VbaModule](../../com.aspose.words/vbamodule/) value.
### get(String name) {#get-java.lang.String}
```
public VbaModule get(String name)
```


Ruft ein [VbaModule](../../com.aspose.words/vbamodule/) Objekt anhand des Namens ab, oder Null, wenn nicht gefunden.

 **Examples:** 

Zeigt, wie man auf die VBA-Projektinformationen eines Dokuments zugreift.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[VbaModule](../../com.aspose.words/vbamodule/) - The corresponding [VbaModule](../../com.aspose.words/vbamodule/) value.
### getCount() {#getCount}
```
public int getCount()
```


Gibt die Anzahl der VBA‑Module in der Sammlung zurück.

 **Examples:** 

Zeigt, wie man auf die VBA-Projektinformationen eines Dokuments zugreift.

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
int – Die Anzahl der VBA‑Module in der Sammlung.
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


Entfernt das angegebene Modul aus der Sammlung.

 **Examples:** 

Zeigt, wie man auf die VBA-Projektinformationen eines Dokuments zugreift.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| module | [VbaModule](../../com.aspose.words/vbamodule/) | Das zu entfernende Modul. |

