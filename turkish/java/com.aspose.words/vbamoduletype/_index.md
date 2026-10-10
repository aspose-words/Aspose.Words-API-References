---
title: "VbaModuleType"
linktitle: "VbaModuleType"
second_title: "Aspose.Words Java için"
description: "Java'da bir VBA projesindeki modelin türünü belirtir."
type: docs
weight: 708
url: /tr/java/com.aspose.words/vbamoduletype/
---

**Inheritance:**
java.lang.Object
```
public class VbaModuleType
```

Bir VBA projesindeki modelin türünü belirtir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CLASS_MODULE](#CLASS-MODULE) | Yeni bir nesne için tanımı içeren bir modül. |
| [DESIGNER_MODULE](#DESIGNER-MODULE) | Projeye kaydedilmiş bir ActiveX denetiminin yöntem ve özelliklerini genişleten bir VBA modülü. |
| [DOCUMENT_MODULE](#DOCUMENT-MODULE) | Bir belgeyle ilişkili gömülü makrolar ve programatik erişim işlemleri için bir modül belirten bir VBA proje öğesi türü. |
| [PROCEDURAL_MODULE](#PROCEDURAL-MODULE) | Alt yordamlar ve işlevlerden oluşan bir koleksiyon. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String vbaModuleTypeName)](#fromName-java.lang.String) |  |
| [getName(int vbaModuleType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int vbaModuleType)](#toString-int) |  |
### CLASS_MODULE {#CLASS-MODULE}
```
public static int CLASS_MODULE
```


Yeni bir nesne için tanımı içeren bir modül. Bir sınıfın her örneği yeni bir nesne oluşturur ve modülde tanımlanan prosedürler nesnenin özellikleri ve yöntemleri haline gelir.

### DESIGNER_MODULE {#DESIGNER-MODULE}
```
public static int DESIGNER_MODULE
```


Projeye kaydedilmiş bir ActiveX denetiminin yöntem ve özelliklerini genişleten bir VBA modülü.

### DOCUMENT_MODULE {#DOCUMENT-MODULE}
```
public static int DOCUMENT_MODULE
```


Bir belgeyle ilişkili gömülü makrolar ve programatik erişim işlemleri için bir modül belirten bir VBA proje öğesi türü.

### PROCEDURAL_MODULE {#PROCEDURAL-MODULE}
```
public static int PROCEDURAL_MODULE
```


Alt yordamlar ve işlevlerden oluşan bir koleksiyon.

### length {#length}
```
public static int length
```


### fromName(String vbaModuleTypeName) {#fromName-java.lang.String}
```
public static int fromName(String vbaModuleTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| vbaModuleTypeName | java.lang.String |  |

**Returns:**
int
### getName(int vbaModuleType) {#getName-int}
```
public static String getName(int vbaModuleType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| vbaModuleType | int |  |

**Returns:**
java.lang.String
