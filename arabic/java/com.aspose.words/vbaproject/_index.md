---
title: "VbaProject"
linktitle: "VbaProject"
second_title: "Aspose.Words لـ Java"
description: "يوفر الوصول إلى معلومات مشروع VBA في Java."
type: docs
weight: 709
url: /ar/java/com.aspose.words/vbaproject/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class VbaProject implements Cloneable
```

يوفر الوصول إلى معلومات مشروع VBA. يُعرَّف مشروع VBA داخل المستند على أنه مجموعة من وحدات VBA.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with VBA Macros ][Working with VBA Macros].

 **Examples:** 

يعرض كيفية الوصول إلى معلومات مشروع VBA للمستند.

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
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [VbaProject()](#VbaProject) | ينشئ [VbaProject](../../com.aspose.words/vbaproject/) فارغًا. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [deepClone()](#deepClone) | ينفّذ نسخة من [VbaProject](../../com.aspose.words/vbaproject/). |
| [getCodePage()](#getCodePage) | يحصل على صفحة الترميز لمشروع VBA\u2019s. |
| [getModules()](#getModules) | يعيد مجموعة من وحدات مشروع VBA. |
| [getName()](#getName) | يحصل على اسم مشروع VBA. |
| [getReferences()](#getReferences) | يحصل على مجموعة من مراجع مشروع VBA. |
| [isProtected()](#isProtected) | يظهر ما إذا كان [VbaProject](../../com.aspose.words/vbaproject/) محميًا بكلمة مرور. |
| [isSigned()](#isSigned) | يظهر ما إذا كان [VbaProject](../../com.aspose.words/vbaproject/) موقّعًا أم لا. |
| [setCodePage(int value)](#setCodePage-int) | يضبط صفحة الترميز لمشروع VBA\u2019s. |
| [setName(String value)](#setName-java.lang.String) | يضبط اسم مشروع VBA. |
### VbaProject() {#VbaProject}
```
public VbaProject()
```


ينشئ [VbaProject](../../com.aspose.words/vbaproject/) فارغًا.

 **Examples:** 

يعرض كيفية إنشاء مشروع VBA باستخدام الماكرو.

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


ينفّذ نسخة من [VbaProject](../../com.aspose.words/vbaproject/).

 **Examples:** 

يوضح كيفية استنساخ عميق لمشروع VBA والوحدة.

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


يحصل على صفحة الترميز لمشروع VBA\u2019s.

 **Remarks:** 

يرجى ملاحظة أن VBA ميزة ما قبل Unicode ويجب عليك ضبط صفحة الترميز المناسبة صراحةً للحفاظ على مجموعات الأحرف الإقليمية.

 **Examples:** 

يعرض كيفية الوصول إلى معلومات مشروع VBA للمستند.

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
int - صفحة الترميز لمشروع VBA\u2019s.
### getModules() {#getModules}
```
public VbaModuleCollection getModules()
```


يعيد مجموعة من وحدات مشروع VBA.

 **Examples:** 

يعرض كيفية الوصول إلى معلومات مشروع VBA للمستند.

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


يحصل على اسم مشروع VBA.

 **Examples:** 

يعرض كيفية الوصول إلى معلومات مشروع VBA للمستند.

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

يعرض كيفية إنشاء مشروع VBA باستخدام الماكرو.

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
java.lang.String - اسم مشروع VBA.
### getReferences() {#getReferences}
```
public VbaReferenceCollection getReferences()
```


يحصل على مجموعة من مراجع مشروع VBA.

 **Examples:** 

يظهر كيفية الحصول على/إزالة عنصر من مجموعة مراجع VBA.

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


يظهر ما إذا كان [VbaProject](../../com.aspose.words/vbaproject/) محميًا بكلمة مرور.

 **Examples:** 

يظهر ما إذا كان VbaProject محميًا بكلمة مرور.

```

 Document doc = new Document(getMyDir() + "Vba protected.docm");
 Assert.assertTrue(doc.getVbaProject().isProtected());
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### isSigned() {#isSigned}
```
public boolean isSigned()
```


يظهر ما إذا كان [VbaProject](../../com.aspose.words/vbaproject/) موقّعًا أم لا.

 **Examples:** 

يعرض كيفية الوصول إلى معلومات مشروع VBA للمستند.

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
boolean - القيمة المنطقية المقابلة.
### setCodePage(int value) {#setCodePage-int}
```
public void setCodePage(int value)
```


يضبط صفحة الترميز لمشروع VBA\u2019s.

 **Remarks:** 

يرجى ملاحظة أن VBA ميزة ما قبل Unicode ويجب عليك ضبط صفحة الترميز المناسبة صراحةً للحفاظ على مجموعات الأحرف الإقليمية.

 **Examples:** 

يعرض كيفية الوصول إلى معلومات مشروع VBA للمستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | صفحة الترميز لمشروع VBA. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


يضبط اسم مشروع VBA.

 **Examples:** 

يعرض كيفية الوصول إلى معلومات مشروع VBA للمستند.

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

يعرض كيفية إنشاء مشروع VBA باستخدام الماكرو.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم مشروع VBA. |

