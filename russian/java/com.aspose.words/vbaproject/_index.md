---
title: "VbaProject"
linktitle: "VbaProject"
second_title: "Aspose.Words для Java"
description: "Обеспечивает доступ к информации проекта VBA в Java."
type: docs
weight: 709
url: /ru/java/com.aspose.words/vbaproject/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class VbaProject implements Cloneable
```

Обеспечивает доступ к информации проекта VBA. VBA‑проект в документе определяется как набор модулей VBA.

Чтобы узнать больше, посетите статью документации [ Working with VBA Macros ][Working with VBA Macros].

 **Examples:** 

Показывает, как получить доступ к информации о VBA‑проекте документа.

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
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [VbaProject()](#VbaProject) | Создаёт пустой [VbaProject](../../com.aspose.words/vbaproject/). |
## Методы

| Метод | Описание |
| --- | --- |
| [deepClone()](#deepClone) | Выполняет копирование [VbaProject](../../com.aspose.words/vbaproject/). |
| [getCodePage()](#getCodePage) | Получает кодовую страницу проекта VBA\\u2019s. |
| [getModules()](#getModules) | Возвращает коллекцию модулей проекта VBA. |
| [getName()](#getName) | Получает имя проекта VBA. |
| [getReferences()](#getReferences) | Получает коллекцию ссылок проекта VBA. |
| [isProtected()](#isProtected) | Показывает, защищён ли [VbaProject](../../com.aspose.words/vbaproject/) паролем. |
| [isSigned()](#isSigned) | Показывает, подписан ли [VbaProject](../../com.aspose.words/vbaproject/) или нет. |
| [setCodePage(int value)](#setCodePage-int) | Устанавливает кодовую страницу проекта VBA\\u2019s. |
| [setName(String value)](#setName-java.lang.String) | Устанавливает имя проекта VBA. |
### VbaProject() {#VbaProject}
```
public VbaProject()
```


Создаёт пустой [VbaProject](../../com.aspose.words/vbaproject/).

 **Examples:** 

Показывает, как создать проект VBA с использованием макросов.

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


Выполняет копирование [VbaProject](../../com.aspose.words/vbaproject/).

 **Examples:** 

Показывает, как глубоко клонировать проект VBA и модуль.

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


Получает кодовую страницу проекта VBA\\u2019s.

 **Remarks:** 

Обратите внимание, что VBA — это пред-Unicode функция, и вам необходимо явно установить соответствующую кодовую страницу для сохранения региональных наборов символов.

 **Examples:** 

Показывает, как получить доступ к информации о VBA‑проекте документа.

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
int — кодовая страница проекта VBA\\u2019s.
### getModules() {#getModules}
```
public VbaModuleCollection getModules()
```


Возвращает коллекцию модулей проекта VBA.

 **Examples:** 

Показывает, как получить доступ к информации о VBA‑проекте документа.

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


Получает имя проекта VBA.

 **Examples:** 

Показывает, как получить доступ к информации о VBA‑проекте документа.

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

Показывает, как создать проект VBA с использованием макросов.

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
java.lang.String — имя проекта VBA.
### getReferences() {#getReferences}
```
public VbaReferenceCollection getReferences()
```


Получает коллекцию ссылок проекта VBA.

 **Examples:** 

Показывает, как получить/удалить элемент из коллекции ссылок VBA.

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


Показывает, защищён ли [VbaProject](../../com.aspose.words/vbaproject/) паролем.

 **Examples:** 

Показывает, защищён ли VbaProject паролем.

```

 Document doc = new Document(getMyDir() + "Vba protected.docm");
 Assert.assertTrue(doc.getVbaProject().isProtected());
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### isSigned() {#isSigned}
```
public boolean isSigned()
```


Показывает, подписан ли [VbaProject](../../com.aspose.words/vbaproject/) или нет.

 **Examples:** 

Показывает, как получить доступ к информации о VBA‑проекте документа.

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
boolean - Соответствующее  boolean  значение.
### setCodePage(int value) {#setCodePage-int}
```
public void setCodePage(int value)
```


Устанавливает кодовую страницу проекта VBA\\u2019s.

 **Remarks:** 

Обратите внимание, что VBA — это пред-Unicode функция, и вам необходимо явно установить соответствующую кодовую страницу для сохранения региональных наборов символов.

 **Examples:** 

Показывает, как получить доступ к информации о VBA‑проекте документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Кодовая страница проекта VBA. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Устанавливает имя проекта VBA.

 **Examples:** 

Показывает, как получить доступ к информации о VBA‑проекте документа.

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

Показывает, как создать проект VBA с использованием макросов.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя проекта VBA. |

