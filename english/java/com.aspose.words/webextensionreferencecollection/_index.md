---
title: WebExtensionReferenceCollection
linktitle: WebExtensionReferenceCollection
second_title: Aspose.Words for Java API Reference
description: Specifies a list of web extension references in Java.
type: docs
weight: 627
url: /java/com.aspose.words/webextensionreferencecollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.BaseWebExtensionCollection](../../com.aspose.words/basewebextensioncollection/)
```
public class WebExtensionReferenceCollection extends BaseWebExtensionCollection
```

Specifies a list of web extension references.

To learn more, visit the [ Work with Office Add-ins ][Work with Office Add-ins] documentation article.


[Work with Office Add-ins]: https://docs.aspose.com/words/java/work-with-office-add-ins/
## Methods

| Method | Description |
| --- | --- |
| [clear()](#clear) | Removes all elements from the collection. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(int index)](#get-int) | Gets an item at the specified index. |
| [getClass()](#getClass) |  |
| [getCount()](#getCount) | Gets the number of elements contained in the collection. |
| [hashCode()](#hashCode) |  |
| [iterator()](#iterator) | Returns an enumerator that can iterate through a collection. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove(int index)](#remove-int) | Removes the item at the specified index from the collection. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### clear() {#clear}
```
public void clear()
```


Removes all elements from the collection.

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
### get(int index) {#get-int}
```
public Object get(int index)
```


Gets an item at the specified index.

 **Examples:** 

Shows how to work with a document's collection of web extensions.

```

 Document doc = new Document(getMyDir() + "Web extension.docx");

 Assert.assertEquals(1, doc.getWebExtensionTaskPanes().getCount());

 // Print all properties of the document's web extension.
 WebExtensionPropertyCollection webExtensionPropertyCollection = doc.getWebExtensionTaskPanes().get(0).getWebExtension().getProperties();
 Iterator enumerator = webExtensionPropertyCollection.iterator();

 while (enumerator.hasNext()) {
     WebExtensionProperty webExtensionProperty = enumerator.next();
     System.out.println("Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
 }

 // Remove the web extension.
 doc.getWebExtensionTaskPanes().remove(0);

 Assert.assertEquals(0, doc.getWebExtensionTaskPanes().getCount());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the item. |

**Returns:**
java.lang.Object - An item at the specified index.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of elements contained in the collection.

 **Examples:** 

Shows how to work with a document's collection of web extensions.

```

 Document doc = new Document(getMyDir() + "Web extension.docx");

 Assert.assertEquals(1, doc.getWebExtensionTaskPanes().getCount());

 // Print all properties of the document's web extension.
 WebExtensionPropertyCollection webExtensionPropertyCollection = doc.getWebExtensionTaskPanes().get(0).getWebExtension().getProperties();
 Iterator enumerator = webExtensionPropertyCollection.iterator();

 while (enumerator.hasNext()) {
     WebExtensionProperty webExtensionProperty = enumerator.next();
     System.out.println("Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
 }

 // Remove the web extension.
 doc.getWebExtensionTaskPanes().remove(0);

 Assert.assertEquals(0, doc.getWebExtensionTaskPanes().getCount());
 
```

**Returns:**
int - The number of elements contained in the collection.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an enumerator that can iterate through a collection.

 **Examples:** 

Shows how to work with a document's collection of web extensions.

```

 Document doc = new Document(getMyDir() + "Web extension.docx");

 Assert.assertEquals(1, doc.getWebExtensionTaskPanes().getCount());

 // Print all properties of the document's web extension.
 WebExtensionPropertyCollection webExtensionPropertyCollection = doc.getWebExtensionTaskPanes().get(0).getWebExtension().getProperties();
 Iterator enumerator = webExtensionPropertyCollection.iterator();

 while (enumerator.hasNext()) {
     WebExtensionProperty webExtensionProperty = enumerator.next();
     System.out.println("Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
 }

 // Remove the web extension.
 doc.getWebExtensionTaskPanes().remove(0);

 Assert.assertEquals(0, doc.getWebExtensionTaskPanes().getCount());
 
```

**Returns:**
java.util.Iterator - 
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### remove(int index) {#remove-int}
```
public void remove(int index)
```


Removes the item at the specified index from the collection.

 **Examples:** 

Shows how to work with a document's collection of web extensions.

```

 Document doc = new Document(getMyDir() + "Web extension.docx");

 Assert.assertEquals(1, doc.getWebExtensionTaskPanes().getCount());

 // Print all properties of the document's web extension.
 WebExtensionPropertyCollection webExtensionPropertyCollection = doc.getWebExtensionTaskPanes().get(0).getWebExtension().getProperties();
 Iterator enumerator = webExtensionPropertyCollection.iterator();

 while (enumerator.hasNext()) {
     WebExtensionProperty webExtensionProperty = enumerator.next();
     System.out.println("Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
 }

 // Remove the web extension.
 doc.getWebExtensionTaskPanes().remove(0);

 Assert.assertEquals(0, doc.getWebExtensionTaskPanes().getCount());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the collection item. |

### toString() {#toString}
```
public String toString()
```




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

