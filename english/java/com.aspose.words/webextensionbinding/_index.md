---
title: WebExtensionBinding
linktitle: WebExtensionBinding
second_title: Aspose.Words for Java
description: Specifies a binding relationship between a web extension and the data in the document in Java.
type: docs
weight: 674
url: /java/com.aspose.words/webextensionbinding/
---

**Inheritance:**
java.lang.Object
```
public class WebExtensionBinding
```

Specifies a binding relationship between a web extension and the data in the document.

To learn more, visit the [ Work with Office Add-ins ][Work with Office Add-ins] documentation article.


[Work with Office Add-ins]: https://docs.aspose.com/words/java/work-with-office-add-ins/
## Constructors

| Constructor | Description |
| --- | --- |
| [WebExtensionBinding(String id, int bindingType, String appRef)](#WebExtensionBinding-java.lang.String-int-java.lang.String) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getAppRef()](#getAppRef) | Specifies the binding key used to map the binding entry in this list with the bound data in the document. |
| [getBindingType()](#getBindingType) | Specifies the binding type. |
| [getId()](#getId) | Specifies the binding identifier. |
| [setAppRef(String value)](#setAppRef-java.lang.String) | Specifies the binding key used to map the binding entry in this list with the bound data in the document. |
| [setBindingType(int value)](#setBindingType-int) | Specifies the binding type. |
| [setId(String value)](#setId-java.lang.String) | Specifies the binding identifier. |
### WebExtensionBinding(String id, int bindingType, String appRef) {#WebExtensionBinding-java.lang.String-int-java.lang.String}
```
public WebExtensionBinding(String id, int bindingType, String appRef)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| id | java.lang.String |  |
| bindingType | int |  |
| appRef | java.lang.String |  |

### getAppRef() {#getAppRef}
```
public String getAppRef()
```


Specifies the binding key used to map the binding entry in this list with the bound data in the document.

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

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getBindingType() {#getBindingType}
```
public int getBindingType()
```


Specifies the binding type.

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

**Returns:**
int - The corresponding  int  value. The returned value is one of [WebExtensionBindingType](../../com.aspose.words/webextensionbindingtype/) constants.
### getId() {#getId}
```
public String getId()
```


Specifies the binding identifier.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setAppRef(String value) {#setAppRef-java.lang.String}
```
public void setAppRef(String value)
```


Specifies the binding key used to map the binding entry in this list with the bound data in the document.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setBindingType(int value) {#setBindingType-int}
```
public void setBindingType(int value)
```


Specifies the binding type.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [WebExtensionBindingType](../../com.aspose.words/webextensionbindingtype/) constants. |

### setId(String value) {#setId-java.lang.String}
```
public void setId(String value)
```


Specifies the binding identifier.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

