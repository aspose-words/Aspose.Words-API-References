---
title: "WebExtensionStoreType"
linktitle: "WebExtensionStoreType"
second_title: "Aspose.Words لـ Java"
description: "يسرد الأنواع المتاحة لمخزن امتداد الويب في جافا."
type: docs
weight: 734
url: /ar/java/com.aspose.words/webextensionstoretype/
---

**Inheritance:**
java.lang.Object
```
public class WebExtensionStoreType
```

يسرد الأنواع المتاحة لمخزن امتداد ويب.

 **Examples:** 

يوضح كيفية إضافة امتداد ويب إلى مستند.

```

 Document doc = new Document();

 // Create task pane with "MyScript" add-in, which will be used by the document,
 // then set its default location.
 TaskPane myScriptTaskPane = new TaskPane();
 doc.getWebExtensionTaskPanes().add(myScriptTaskPane);
 myScriptTaskPane.setDockState(TaskPaneDockState.RIGHT);
 myScriptTaskPane.isVisible(true);
 myScriptTaskPane.setWidth(300.0);
 myScriptTaskPane.isLocked(true);

 // If there are multiple task panes in the same docking location, we can set this index to arrange them.
 myScriptTaskPane.setRow(1);

 // Create an add-in called "MyScript Math Sample", which the task pane will display within.
 WebExtension webExtension = myScriptTaskPane.getWebExtension();

 // Set application store reference parameters for our add-in, such as the ID.
 webExtension.getReference().setId("WA104380646");
 webExtension.getReference().setVersion("1.0.0.0");
 webExtension.getReference().setStoreType(WebExtensionStoreType.OMEX);
 webExtension.getReference().setStore("English (United States)");
 webExtension.getProperties().add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
 webExtension.getBindings().add(new WebExtensionBinding("MyScript", WebExtensionBindingType.TEXT, "104380646"));

 // Allow the user to interact with the add-in.
 webExtension.isFrozen(false);

 // We can access the web extension in Microsoft Word via Developer -> Add-ins.
 doc.save(getArtifactsDir() + "Document.WebExtension.docx");

 // Remove all web extension task panes at once like this.
 doc.getWebExtensionTaskPanes().clear();

 Assert.assertEquals(0, doc.getWebExtensionTaskPanes().getCount());

 doc = new Document(getArtifactsDir() + "Document.WebExtension.docx");

 myScriptTaskPane = doc.getWebExtensionTaskPanes().get(0);
 Assert.assertEquals(TaskPaneDockState.RIGHT, myScriptTaskPane.getDockState());
 Assert.assertTrue(myScriptTaskPane.isVisible());
 Assert.assertEquals(300.0d, myScriptTaskPane.getWidth());
 Assert.assertTrue(myScriptTaskPane.isLocked());
 Assert.assertEquals(1, myScriptTaskPane.getRow());

 webExtension = myScriptTaskPane.getWebExtension();
 Assert.assertEquals("", webExtension.getId());

 Assert.assertEquals("WA104380646", webExtension.getReference().getId());
 Assert.assertEquals("1.0.0.0", webExtension.getReference().getVersion());
 Assert.assertEquals(WebExtensionStoreType.OMEX, webExtension.getReference().getStoreType());
 Assert.assertEquals("English (United States)", webExtension.getReference().getStore());
 Assert.assertEquals(0, webExtension.getAlternateReferences().getCount());

 Assert.assertEquals("MyScript", webExtension.getProperties().get(0).getName());
 Assert.assertEquals("MyScript Math Sample", webExtension.getProperties().get(0).getValue());

 Assert.assertEquals("MyScript", webExtension.getBindings().get(0).getId());
 Assert.assertEquals(WebExtensionBindingType.TEXT, webExtension.getBindings().get(0).getBindingType());
 Assert.assertEquals("104380646", webExtension.getBindings().get(0).getAppRef());

 Assert.assertFalse(webExtension.isFrozen());
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [DEFAULT](#DEFAULT) | القيمة الافتراضية. |
| [EXCHANGE](#EXCHANGE) | يحدد أن نوع المخزن هو خادم Exchange. |
| [EX_CATALOG](#EX-CATALOG) | يحدد أن نوع المتجر هو النشر المركزي عبر Exchange. |
| [FILE_SYSTEM](#FILE-SYSTEM) | يحدد أن نوع المتجر هو مشاركة نظام ملفات. |
| [OMEX](#OMEX) | يحدد أن نوع المتجر هو Office.com. |
| [REGISTRY](#REGISTRY) | يحدد أن نوع المتجر هو سجل النظام. |
| [SP_APP](#SP-APP) |  |
| [SP_CATALOG](#SP-CATALOG) |  |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String webExtensionStoreTypeName)](#fromName-java.lang.String) |  |
| [getName(int webExtensionStoreType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int webExtensionStoreType)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


القيمة الافتراضية.

### EXCHANGE {#EXCHANGE}
```
public static int EXCHANGE
```


يحدد أن نوع المخزن هو خادم Exchange.

### EX_CATALOG {#EX-CATALOG}
```
public static int EX_CATALOG
```


يحدد أن نوع المتجر هو النشر المركزي عبر Exchange.

### FILE_SYSTEM {#FILE-SYSTEM}
```
public static int FILE_SYSTEM
```


يحدد أن نوع المتجر هو مشاركة نظام ملفات.

### OMEX {#OMEX}
```
public static int OMEX
```


يحدد أن نوع المتجر هو Office.com.

### REGISTRY {#REGISTRY}
```
public static int REGISTRY
```


يحدد أن نوع المتجر هو سجل النظام.

### SP_APP {#SP-APP}
```
public static int SP_APP
```


### SP_CATALOG {#SP-CATALOG}
```
public static int SP_CATALOG
```


### length {#length}
```
public static int length
```


### fromName(String webExtensionStoreTypeName) {#fromName-java.lang.String}
```
public static int fromName(String webExtensionStoreTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| webExtensionStoreTypeName | java.lang.String |  |

**Returns:**
int
### getName(int webExtensionStoreType) {#getName-int}
```
public static String getName(int webExtensionStoreType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| webExtensionStoreType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int webExtensionStoreType) {#toString-int}
```
public static String toString(int webExtensionStoreType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| webExtensionStoreType | int |  |

**Returns:**
java.lang.String
