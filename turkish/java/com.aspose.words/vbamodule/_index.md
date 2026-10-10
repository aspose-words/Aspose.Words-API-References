---
title: "VbaModule"
linktitle: "VbaModule"
second_title: "Aspose.Words Java için"
description: "Java'da VBA proje modülüne erişim sağlar."
type: docs
weight: 706
url: /tr/java/com.aspose.words/vbamodule/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class VbaModule implements Cloneable
```

VBA proje modülüne erişim sağlar.

Daha fazla bilgi için, [ Working with VBA Macros ][Working with VBA Macros] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir belgenin VBA proje bilgilerine erişmenin nasıl yapılacağını gösterir.

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
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [VbaModule()](#VbaModule) | Boş bir modül oluşturur. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [deepClone()](#deepClone) | [VbaModule](../../com.aspose.words/vbamodule/) kopyasını gerçekleştirir. |
| [getName()](#getName) | VBA proje modülünün adını alır. |
| [getSourceCode()](#getSourceCode) | VBA proje modülünün kaynak kodunu alır. |
| [getType()](#getType) | Modülün prosedür modülü, belge modülü, sınıf modülü veya tasarımcı modülü olup olmadığını belirtir. |
| [setName(String value)](#setName-java.lang.String) | VBA proje modülünün adını ayarlar. |
| [setSourceCode(String value)](#setSourceCode-java.lang.String) | VBA proje modülünün kaynak kodunu ayarlar. |
| [setType(int value)](#setType-int) | Modülün prosedür modülü, belge modülü, sınıf modülü veya tasarımcı modülü olup olmadığını belirtir. |
### VbaModule() {#VbaModule}
```
public VbaModule()
```


Boş bir modül oluşturur.

 **Examples:** 

Makrolar kullanarak bir VBA projesi oluşturmayı gösterir.

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

### deepClone() {#deepClone}
```
public VbaModule deepClone()
```


[VbaModule](../../com.aspose.words/vbamodule/) kopyasını gerçekleştirir.

 **Examples:** 

Bir VBA projesi ve modülünün derin kopyasını nasıl oluşturacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "VBA project.docm");
 Document destDoc = new Document();

 VbaProject copyVbaProject = doc.getVbaProject().deepClone();
 destDoc.setVbaProject(copyVbaProject);

 // In the destination document, we already have a module named "Module1"
 // because we cloned it along with the project. We will need to remove the module.
 VbaModule oldVbaModule = destDoc.getVbaProject().getModules().get("Module1");
 VbaModule copyVbaModule = doc.getVbaProject().getModules().get("Module1").deepClone();
 destDoc.getVbaProject().getModules().remove(oldVbaModule);
 destDoc.getVbaProject().getModules().add(copyVbaModule);

 destDoc.save(getArtifactsDir() + "VbaProject.CloneVbaProject.docm");
 
```

**Returns:**
[VbaModule](../../com.aspose.words/vbamodule/) - The cloned [VbaModule](../../com.aspose.words/vbamodule/).
### getName() {#getName}
```
public String getName()
```


VBA proje modülünün adını alır.

 **Examples:** 

Bir belgenin VBA proje bilgilerine erişmenin nasıl yapılacağını gösterir.

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

Makrolar kullanarak bir VBA projesi oluşturmayı gösterir.

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

**Returns:**
java.lang.String - VBA proje modülünün adı.
### getSourceCode() {#getSourceCode}
```
public String getSourceCode()
```


VBA proje modülünün kaynak kodunu alır.

 **Examples:** 

Bir belgenin VBA proje bilgilerine erişmenin nasıl yapılacağını gösterir.

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

Makrolar kullanarak bir VBA projesi oluşturmayı gösterir.

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

**Returns:**
java.lang.String - VBA proje modülünün kaynak kodu.
### getType() {#getType}
```
public int getType()
```


Modülün prosedür modülü, belge modülü, sınıf modülü veya tasarımcı modülü olup olmadığını belirtir.

 **Examples:** 

Makrolar kullanarak bir VBA projesi oluşturmayı gösterir.

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

**Returns:**
int - İlgili  int  değeri. Döndürülen değer, [VbaModuleType](../../com.aspose.words/vbamoduletype/) sabitlerinden biridir.
### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


VBA proje modülünün adını ayarlar.

 **Examples:** 

Bir belgenin VBA proje bilgilerine erişmenin nasıl yapılacağını gösterir.

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

Makrolar kullanarak bir VBA projesi oluşturmayı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | VBA proje modülünün adı. |

### setSourceCode(String value) {#setSourceCode-java.lang.String}
```
public void setSourceCode(String value)
```


VBA proje modülünün kaynak kodunu ayarlar.

 **Examples:** 

Bir belgenin VBA proje bilgilerine erişmenin nasıl yapılacağını gösterir.

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

Makrolar kullanarak bir VBA projesi oluşturmayı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | VBA proje modülünün kaynak kodu. |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


Modülün prosedür modülü, belge modülü, sınıf modülü veya tasarımcı modülü olup olmadığını belirtir.

 **Examples:** 

Makrolar kullanarak bir VBA projesi oluşturmayı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [VbaModuleType](../../com.aspose.words/vbamoduletype/) sabitlerinden biri olmalıdır. |

