---
title: "VbaModule"
linktitle: "VbaModule"
second_title: "Aspose.Words لـ Java"
description: "يوفر الوصول إلى وحدة مشروع VBA في Java."
type: docs
weight: 706
url: /ar/java/com.aspose.words/vbamodule/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class VbaModule implements Cloneable
```

يوفر الوصول إلى وحدة مشروع VBA.

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
| [VbaModule()](#VbaModule) | ينشئ وحدة فارغة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [deepClone()](#deepClone) | ينفذ نسخة من [VbaModule](../../com.aspose.words/vbamodule/). |
| [getName()](#getName) | يحصل على اسم وحدة مشروع VBA. |
| [getSourceCode()](#getSourceCode) | يحصل على شفرة المصدر لوحدة مشروع VBA. |
| [getType()](#getType) | يحدد ما إذا كانت الوحدة وحدة إجرائية، أو وحدة مستند، أو وحدة فئة، أو وحدة مصمم. |
| [setName(String value)](#setName-java.lang.String) | يضبط اسم وحدة مشروع VBA. |
| [setSourceCode(String value)](#setSourceCode-java.lang.String) | يضبط شفرة المصدر لوحدة مشروع VBA. |
| [setType(int value)](#setType-int) | يحدد ما إذا كانت الوحدة وحدة إجرائية، أو وحدة مستند، أو وحدة فئة، أو وحدة مصمم. |
### VbaModule() {#VbaModule}
```
public VbaModule()
```


ينشئ وحدة فارغة.

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
public VbaModule deepClone()
```


ينفذ نسخة من [VbaModule](../../com.aspose.words/vbamodule/).

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
[VbaModule](../../com.aspose.words/vbamodule/) - The cloned [VbaModule](../../com.aspose.words/vbamodule/).
### getName() {#getName}
```
public String getName()
```


يحصل على اسم وحدة مشروع VBA.

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
java.lang.String - اسم وحدة مشروع VBA.
### getSourceCode() {#getSourceCode}
```
public String getSourceCode()
```


يحصل على شفرة المصدر لوحدة مشروع VBA.

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
java.lang.String - شفرة المصدر لوحدة مشروع VBA.
### getType() {#getType}
```
public int getType()
```


يحدد ما إذا كانت الوحدة وحدة إجرائية، أو وحدة مستند، أو وحدة فئة، أو وحدة مصمم.

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

**Returns:**
int - القيمة  int  المقابلة. القيمة المرجعة هي واحدة من ثوابت [VbaModuleType](../../com.aspose.words/vbamoduletype/).
### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


يضبط اسم وحدة مشروع VBA.

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
| قيمة | java.lang.String | اسم وحدة مشروع VBA. |

### setSourceCode(String value) {#setSourceCode-java.lang.String}
```
public void setSourceCode(String value)
```


يضبط شفرة المصدر لوحدة مشروع VBA.

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
| قيمة | java.lang.String | شفرة المصدر لوحدة مشروع VBA. |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


يحدد ما إذا كانت الوحدة وحدة إجرائية، أو وحدة مستند، أو وحدة فئة، أو وحدة مصمم.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة  int  المقابلة. يجب أن تكون القيمة واحدة من ثوابت [VbaModuleType](../../com.aspose.words/vbamoduletype/). |

