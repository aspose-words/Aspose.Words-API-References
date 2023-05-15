---
title: WebExtensionBindingType
linktitle: WebExtensionBindingType
second_title: Aspose.Words for Java
description: Enumerates available types of binding between a web extension and the data in the document in Java.
type: docs
weight: 634
url: /java/com.aspose.words/webextensionbindingtype/
---

**Inheritance:**
java.lang.Object
```
public class WebExtensionBindingType
```

Enumerates available types of binding between a web extension and the data in the document.

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
| [DEFAULT](#DEFAULT) |  |
| [MATRIX](#MATRIX) | Tabular data without a header row. |
| [TABLE](#TABLE) | Tabular data with a header row. |
| [TEXT](#TEXT) | Plain text. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String webExtensionBindingTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int webExtensionBindingType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int webExtensionBindingType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


### MATRIX {#MATRIX}
```
public static int MATRIX
```


Tabular data without a header row.

### TABLE {#TABLE}
```
public static int TABLE
```


Tabular data with a header row.

### TEXT {#TEXT}
```
public static int TEXT
```


Plain text.

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
### fromName(String webExtensionBindingTypeName) {#fromName-java.lang.String}
```
public static int fromName(String webExtensionBindingTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| webExtensionBindingTypeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int webExtensionBindingType) {#getName-int}
```
public static String getName(int webExtensionBindingType)
```




**Parameters:**
| Parameter | Type | Description |
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
### toString(int webExtensionBindingType) {#toString-int}
```
public static String toString(int webExtensionBindingType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| webExtensionBindingType | int |  |

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

