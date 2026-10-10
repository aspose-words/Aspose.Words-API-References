---
title: "VbaModuleCollection"
linktitle: "VbaModuleCollection"
second_title: "Aspose.Words para Java"
description: "Representa una colección de objetos VbaModule en Java."
type: docs
weight: 707
url: /es/java/com.aspose.words/vbamodulecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class VbaModuleCollection implements Iterable
```

Representa una colección de objetos [VbaModule](../../com.aspose.words/vbamodule/).

Para obtener más información, visite el artículo de documentación [ Working with VBA Macros ][Working with VBA Macros].

 **Examples:** 

Muestra cómo acceder a la información del proyecto VBA de un documento.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [add(VbaModule vbaModule)](#add-com.aspose.words.VbaModule) | Agrega un módulo a la colección. |
| [get(int index)](#get-int) | Recupera un objeto [VbaModule](../../com.aspose.words/vbamodule/) por índice. |
| [get(String name)](#get-java.lang.String) | Recupera un objeto [VbaModule](../../com.aspose.words/vbamodule/) por nombre, o Null si no se encuentra. |
| [getCount()](#getCount) | Devuelve el número de módulos VBA en la colección. |
| [iterator()](#iterator) |  |
| [remove(VbaModule module)](#remove-com.aspose.words.VbaModule) | Elimina el módulo especificado de la colección. |
### add(VbaModule vbaModule) {#add-com.aspose.words.VbaModule}
```
public void add(VbaModule vbaModule)
```


Agrega un módulo a la colección.

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| vbaModule | [VbaModule](../../com.aspose.words/vbamodule/) |  |

### get(int index) {#get-int}
```
public VbaModule get(int index)
```


Recupera un objeto [VbaModule](../../com.aspose.words/vbamodule/) por índice.

 **Examples:** 

Muestra cómo acceder a la información del proyecto VBA de un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | Índice basado en cero del módulo a recuperar. |

**Returns:**
[VbaModule](../../com.aspose.words/vbamodule/) - The corresponding [VbaModule](../../com.aspose.words/vbamodule/) value.
### get(String name) {#get-java.lang.String}
```
public VbaModule get(String name)
```


Recupera un objeto [VbaModule](../../com.aspose.words/vbamodule/) por nombre, o Null si no se encuentra.

 **Examples:** 

Muestra cómo acceder a la información del proyecto VBA de un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String |  |

**Returns:**
[VbaModule](../../com.aspose.words/vbamodule/) - The corresponding [VbaModule](../../com.aspose.words/vbamodule/) value.
### getCount() {#getCount}
```
public int getCount()
```


Devuelve el número de módulos VBA en la colección.

 **Examples:** 

Muestra cómo acceder a la información del proyecto VBA de un documento.

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
int - El número de módulos VBA en la colección.
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


Elimina el módulo especificado de la colección.

 **Examples:** 

Muestra cómo acceder a la información del proyecto VBA de un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| module | [VbaModule](../../com.aspose.words/vbamodule/) | El módulo a eliminar. |

