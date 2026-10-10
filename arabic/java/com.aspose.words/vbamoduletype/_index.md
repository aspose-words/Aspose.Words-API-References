---
title: "VbaModuleType"
linktitle: "VbaModuleType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع نموذج في مشروع VBA بلغة Java."
type: docs
weight: 708
url: /ar/java/com.aspose.words/vbamoduletype/
---

**Inheritance:**
java.lang.Object
```
public class VbaModuleType
```

يحدد نوع النموذج في مشروع VBA.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [CLASS_MODULE](#CLASS-MODULE) | وحدة تحتوي على تعريف كائن جديد. |
| [DESIGNER_MODULE](#DESIGNER-MODULE) | وحدة VBA تُوسّع الأساليب والخصائص لعنصر تحكم ActiveX تم تسجيله مع المشروع. |
| [DOCUMENT_MODULE](#DOCUMENT-MODULE) | نوع من عناصر مشروع VBA يحدد وحدة للماكرو المدمج وعمليات الوصول البرمجي المرتبطة بمستند. |
| [PROCEDURAL_MODULE](#PROCEDURAL-MODULE) | مجموعة من الروتينات الفرعية والدوال. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String vbaModuleTypeName)](#fromName-java.lang.String) |  |
| [getName(int vbaModuleType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int vbaModuleType)](#toString-int) |  |
### CLASS_MODULE {#CLASS-MODULE}
```
public static int CLASS_MODULE
```


وحدة تحتوي على تعريف كائن جديد. كل نسخة من الفئة تُنشئ كائنًا جديدًا، والإجراءات المعرفة في الوحدة تصبح خصائص وأساليب للكائن.

### DESIGNER_MODULE {#DESIGNER-MODULE}
```
public static int DESIGNER_MODULE
```


وحدة VBA تُوسّع الأساليب والخصائص لعنصر تحكم ActiveX تم تسجيله مع المشروع.

### DOCUMENT_MODULE {#DOCUMENT-MODULE}
```
public static int DOCUMENT_MODULE
```


نوع من عناصر مشروع VBA يحدد وحدة للماكرو المدمج وعمليات الوصول البرمجي المرتبطة بمستند.

### PROCEDURAL_MODULE {#PROCEDURAL-MODULE}
```
public static int PROCEDURAL_MODULE
```


مجموعة من الروتينات الفرعية والدوال.

### length {#length}
```
public static int length
```


### fromName(String vbaModuleTypeName) {#fromName-java.lang.String}
```
public static int fromName(String vbaModuleTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| vbaModuleTypeName | java.lang.String |  |

**Returns:**
int
### getName(int vbaModuleType) {#getName-int}
```
public static String getName(int vbaModuleType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| vbaModuleType | int |  |

**Returns:**
java.lang.String
