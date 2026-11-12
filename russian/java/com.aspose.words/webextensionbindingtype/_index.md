---
title: "WebExtensionBindingType"
linktitle: "WebExtensionBindingType"
second_title: "Aspose.Words для Java"
description: "Перечисляет доступные типы привязки между веб‑расширением и данными в документе в Java."
type: docs
weight: 729
url: /ru/java/com.aspose.words/webextensionbindingtype/
---

**Inheritance:**
java.lang.Object
```
public class WebExtensionBindingType
```

Перечисляет доступные типы привязки между веб‑расширением и данными в документе.

 **Examples:** 

Показывает, как добавить веб‑расширение в документ.

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
## Поля

| Поле | Описание |
| --- | --- |
| [DEFAULT](#DEFAULT) | Матрица, используемая по умолчанию. |
| [MATRIX](#MATRIX) | Табличные данные без строки заголовка. |
| [TABLE](#TABLE) | Табличные данные со строкой заголовка. |
| [TEXT](#TEXT) | Простой текст. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String webExtensionBindingTypeName)](#fromName-java.lang.String) |  |
| [getName(int webExtensionBindingType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int webExtensionBindingType)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Матрица, используемая по умолчанию.

### MATRIX {#MATRIX}
```
public static int MATRIX
```


Табличные данные без строки заголовка.

### TABLE {#TABLE}
```
public static int TABLE
```


Табличные данные со строкой заголовка.

### TEXT {#TEXT}
```
public static int TEXT
```


Простой текст.

### length {#length}
```
public static int length
```


### fromName(String webExtensionBindingTypeName) {#fromName-java.lang.String}
```
public static int fromName(String webExtensionBindingTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| webExtensionBindingTypeName | java.lang.String |  |

**Returns:**
int
### getName(int webExtensionBindingType) {#getName-int}
```
public static String getName(int webExtensionBindingType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| webExtensionBindingType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int webExtensionBindingType) {#toString-int}
```
public static String toString(int webExtensionBindingType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| webExtensionBindingType | int |  |

**Returns:**
java.lang.String
