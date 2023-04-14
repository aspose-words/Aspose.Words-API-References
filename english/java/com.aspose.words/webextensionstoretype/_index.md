---
title: WebExtensionStoreType
linktitle: WebExtensionStoreType
second_title: Aspose.Words for Java API Reference
description: Enumerates available types of a web extension store in Java.
type: docs
weight: 628
url: /java/com.aspose.words/webextensionstoretype/
---

**Inheritance:**
java.lang.Object
```
public class WebExtensionStoreType
```

Enumerates available types of a web extension store.

 **Examples:** 

Shows how to add a web extension to a document.

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
 
```
## Fields

| Field | Description |
| --- | --- |
| [DEFAULT](#DEFAULT) | Default value. |
| [EXCHANGE](#EXCHANGE) | Specifies that the store type is an Exchange server. |
| [EX_CATALOG](#EX-CATALOG) | Specifies that the store type is Centralized Deployment via Exchange. |
| [FILE_SYSTEM](#FILE-SYSTEM) | Specifies that the store type is a file system share. |
| [OMEX](#OMEX) | Specifies that the store type is Office.com. |
| [REGISTRY](#REGISTRY) | Specifies that the store type is the system registry. |
| [SP_APP](#SP-APP) |  |
| [SP_CATALOG](#SP-CATALOG) |  |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String webExtensionStoreTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int webExtensionStoreType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int webExtensionStoreType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Default value.

### EXCHANGE {#EXCHANGE}
```
public static int EXCHANGE
```


Specifies that the store type is an Exchange server.

### EX_CATALOG {#EX-CATALOG}
```
public static int EX_CATALOG
```


Specifies that the store type is Centralized Deployment via Exchange.

### FILE_SYSTEM {#FILE-SYSTEM}
```
public static int FILE_SYSTEM
```


Specifies that the store type is a file system share.

### OMEX {#OMEX}
```
public static int OMEX
```


Specifies that the store type is Office.com.

### REGISTRY {#REGISTRY}
```
public static int REGISTRY
```


Specifies that the store type is the system registry.

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


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fromName(String webExtensionStoreTypeName) {#fromName-java.lang.String}
```
public static int fromName(String webExtensionStoreTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| webExtensionStoreTypeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int webExtensionStoreType) {#getName-int}
```
public static String getName(int webExtensionStoreType)
```




**Parameters:**
| Parameter | Type | Description |
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
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(int webExtensionStoreType) {#toString-int}
```
public static String toString(int webExtensionStoreType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| webExtensionStoreType | int |  |

**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

