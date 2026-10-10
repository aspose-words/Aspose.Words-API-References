---
title: "VbaProject"
linktitle: "VbaProject"
second_title: "Aspose.Words Java için"
description: "Java'da VBA proje bilgilerine erişim sağlar."
type: docs
weight: 709
url: /tr/java/com.aspose.words/vbaproject/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class VbaProject implements Cloneable
```

VBA proje bilgilerine erişim sağlar. Belgede bulunan bir VBA projesi, VBA modüllerinin bir koleksiyonu olarak tanımlanır.

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
| [VbaProject()](#VbaProject) | Boş bir [VbaProject](../../com.aspose.words/vbaproject/) oluşturur. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [deepClone()](#deepClone) | [VbaProject](../../com.aspose.words/vbaproject/) kopyasını gerçekleştirir. |
| [getCodePage()](#getCodePage) | VBA projesinin kod sayfasını alır. |
| [getModules()](#getModules) | VBA proje modüllerinin koleksiyonunu döndürür. |
| [getName()](#getName) | VBA proje adını alır. |
| [getReferences()](#getReferences) | VBA proje referanslarının bir koleksiyonunu alır. |
| [isProtected()](#isProtected) | [VbaProject](../../com.aspose.words/vbaproject/) şifre korumalı olup olmadığını gösterir. |
| [isSigned()](#isSigned) | [VbaProject](../../com.aspose.words/vbaproject/) imzalı olup olmadığını gösterir. |
| [setCodePage(int value)](#setCodePage-int) | VBA projesinin kod sayfasını ayarlar. |
| [setName(String value)](#setName-java.lang.String) | VBA proje adını ayarlar. |
### VbaProject() {#VbaProject}
```
public VbaProject()
```


Boş bir [VbaProject](../../com.aspose.words/vbaproject/) oluşturur.

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
public VbaProject deepClone()
```


[VbaProject](../../com.aspose.words/vbaproject/) kopyasını gerçekleştirir.

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
[VbaProject](../../com.aspose.words/vbaproject/) - The cloned [VbaProject](../../com.aspose.words/vbaproject/).
### getCodePage() {#getCodePage}
```
public int getCodePage()
```


VBA projesinin kod sayfasını alır.

 **Remarks:** 

Lütfen VBA'nın Unicode öncesi bir özellik olduğunu ve bölgesel karakter setlerini korumak için uygun kod sayfasını açıkça ayarlamanız gerektiğini unutmayın.

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
int - VBA projesinin kod sayfası.
### getModules() {#getModules}
```
public VbaModuleCollection getModules()
```


VBA proje modüllerinin koleksiyonunu döndürür.

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
[VbaModuleCollection](../../com.aspose.words/vbamodulecollection/) - Collection of VBA project modules.
### getName() {#getName}
```
public String getName()
```


VBA proje adını alır.

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
java.lang.String - VBA proje adı.
### getReferences() {#getReferences}
```
public VbaReferenceCollection getReferences()
```


VBA proje referanslarının bir koleksiyonunu alır.

 **Examples:** 

VBA referans koleksiyonundan bir elemanı almayı/kaldırmayı nasıl yapacağınızı gösterir.

```

 public void removeVbaReference() throws Exception {
     final String BROKEN_PATH = "X:\\broken.dll";
     Document doc = new Document(getMyDir() + "VBA project.docm");

     VbaReferenceCollection references = doc.getVbaProject().getReferences();
     Assert.assertEquals(5, references.getCount());

     for (int i = references.getCount() - 1; i >= 0; i--) {
         VbaReference reference = doc.getVbaProject().getReferences().get(i);
         String path = getLibIdPath(reference);

         if (BROKEN_PATH.equals(path))
             references.removeAt(i);
     }
     Assert.assertEquals(4, references.getCount());

     references.remove(references.get(1));
     Assert.assertEquals(3, references.getCount());

     doc.save(getArtifactsDir() + "VbaProject.RemoveVbaReference.docm");
 }

 /// 
 /// Returns string representing LibId path of a specified reference.
 /// 
 private static String getLibIdPath(VbaReference reference) {
     switch (reference.getType()) {
         case VbaReferenceType.REGISTERED:
         case VbaReferenceType.ORIGINAL:
         case VbaReferenceType.CONTROL:
             return getLibIdReferencePath(reference.getLibId());
         case VbaReferenceType.PROJECT:
             return getLibIdProjectPath(reference.getLibId());
         default:
             throw new IllegalArgumentException();
     }
 }

 /// 
 /// Returns path from a specified identifier of an Automation type library.
 /// 
 private static String getLibIdReferencePath(String libIdReference) {
     if (libIdReference != null) {
         String[] refParts = libIdReference.split("#");
         if (refParts.length > 3)
             return refParts[3];
     }

     return "";
 }

 /// 
 /// Returns path from a specified identifier of an Automation type library.
 /// 
 private static String getLibIdProjectPath(String libIdProject) {
     return libIdProject != null ? libIdProject.substring(3) : "";
 }
 
```

**Returns:**
[VbaReferenceCollection](../../com.aspose.words/vbareferencecollection/) - A collection of VBA project references.
### isProtected() {#isProtected}
```
public boolean isProtected()
```


[VbaProject](../../com.aspose.words/vbaproject/) şifre korumalı olup olmadığını gösterir.

 **Examples:** 

VbaProject'in şifre korumalı olup olmadığını gösterir.

```

 Document doc = new Document(getMyDir() + "Vba protected.docm");
 Assert.assertTrue(doc.getVbaProject().isProtected());
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### isSigned() {#isSigned}
```
public boolean isSigned()
```


[VbaProject](../../com.aspose.words/vbaproject/) imzalı olup olmadığını gösterir.

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
boolean - İlgili  boolean  değeri.
### setCodePage(int value) {#setCodePage-int}
```
public void setCodePage(int value)
```


VBA projesinin kod sayfasını ayarlar.

 **Remarks:** 

Lütfen VBA'nın Unicode öncesi bir özellik olduğunu ve bölgesel karakter setlerini korumak için uygun kod sayfasını açıkça ayarlamanız gerektiğini unutmayın.

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
| değer | int | VBA projesinin kod sayfası. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


VBA proje adını ayarlar.

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
| değer | java.lang.String | VBA projesi adı. |

