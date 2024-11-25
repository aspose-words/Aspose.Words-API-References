---
title: WebExtensionProperty
linktitle: WebExtensionProperty
second_title: Aspose.Words for Java
description: Specifies a web extension custom property in Java.
type: docs
weight: 685
url: /java/com.aspose.words/webextensionproperty/
---

**Inheritance:**
java.lang.Object
```
public class WebExtensionProperty
```

Specifies a web extension custom property.

To learn more, visit the [ Work with Office Add-ins ][Work with Office Add-ins] documentation article.


[Work with Office Add-ins]: https://docs.aspose.com/words/java/work-with-office-add-ins/
## Constructors

| Constructor | Description |
| --- | --- |
| [WebExtensionProperty(String name, String value)](#WebExtensionProperty-java.lang.String-java.lang.String) | Creates web extension custom property with specified name and value. |
## Methods

| Method | Description |
| --- | --- |
| [getName()](#getName) | Specifies a custom property name |
| [getValue()](#getValue) | Specifies a custom property value. |
| [setName(String value)](#setName-java.lang.String) | Specifies a custom property name |
| [setValue(String value)](#setValue-java.lang.String) | Specifies a custom property value. |
### WebExtensionProperty(String name, String value) {#WebExtensionProperty-java.lang.String-java.lang.String}
```
public WebExtensionProperty(String name, String value)
```


Creates web extension custom property with specified name and value.

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
| name | java.lang.String | Property name. |
| value | java.lang.String | Property value. |

### getName() {#getName}
```
public String getName()
```


Specifies a custom property name

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getValue() {#getValue}
```
public String getValue()
```


Specifies a custom property value.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Specifies a custom property name

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setValue(String value) {#setValue-java.lang.String}
```
public void setValue(String value)
```


Specifies a custom property value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

