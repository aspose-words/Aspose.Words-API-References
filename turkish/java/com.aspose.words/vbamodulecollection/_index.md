---
title: "VbaModuleCollection"
linktitle: "VbaModuleCollection"
second_title: "Aspose.Words Java için"
description: "Java'da VbaModule nesnelerinin bir koleksiyonunu temsil eder."
type: docs
weight: 707
url: /tr/java/com.aspose.words/vbamodulecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class VbaModuleCollection implements Iterable
```

Bir [VbaModule](../../com.aspose.words/vbamodule/) nesnelerinin koleksiyonunu temsil eder.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [add(VbaModule vbaModule)](#add-com.aspose.words.VbaModule) | Koleksiyona bir modül ekler. |
| [get(int index)](#get-int) | Bir [VbaModule](../../com.aspose.words/vbamodule/) nesnesini indeks ile alır. |
| [get(String name)](#get-java.lang.String) | Bir [VbaModule](../../com.aspose.words/vbamodule/) nesnesini ada göre alır, bulunamazsa Null döner. |
| [getCount()](#getCount) | Koleksiyondaki VBA modüllerinin sayısını döndürür. |
| [iterator()](#iterator) |  |
| [remove(VbaModule module)](#remove-com.aspose.words.VbaModule) | Belirtilen modülü koleksiyondan kaldırır. |
### add(VbaModule vbaModule) {#add-com.aspose.words.VbaModule}
```
public void add(VbaModule vbaModule)
```


Koleksiyona bir modül ekler.

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
| vbaModule | [VbaModule](../../com.aspose.words/vbamodule/) |  |

### get(int index) {#get-int}
```
public VbaModule get(int index)
```


Bir [VbaModule](../../com.aspose.words/vbamodule/) nesnesini indeks ile alır.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Alınacak modülün sıfır tabanlı indeksi. |

**Returns:**
[VbaModule](../../com.aspose.words/vbamodule/) - The corresponding [VbaModule](../../com.aspose.words/vbamodule/) value.
### get(String name) {#get-java.lang.String}
```
public VbaModule get(String name)
```


Bir [VbaModule](../../com.aspose.words/vbamodule/) nesnesini ada göre alır, bulunamazsa Null döner.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[VbaModule](../../com.aspose.words/vbamodule/) - The corresponding [VbaModule](../../com.aspose.words/vbamodule/) value.
### getCount() {#getCount}
```
public int getCount()
```


Koleksiyondaki VBA modüllerinin sayısını döndürür.

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

**Returns:**
int - Koleksiyondaki VBA modüllerinin sayısı.
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


Belirtilen modülü koleksiyondan kaldırır.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| module | [VbaModule](../../com.aspose.words/vbamodule/) | Kaldırılacak modül. |

