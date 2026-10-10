---
title: "TaskPaneCollection"
linktitle: "TaskPaneCollection"
second_title: "Aspose.Words für Java"
description: "Gibt eine Liste von persistierten TaskPane-Objekten in Java an."
type: docs
weight: 664
url: /de/java/com.aspose.words/taskpanecollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.BaseWebExtensionCollection](../../com.aspose.words/basewebextensioncollection/)
```
public class TaskPaneCollection extends BaseWebExtensionCollection
```

Gibt eine Liste von persistierten Task‑Pane‑Objekten an.

Weitere Informationen finden Sie im Dokumentationsartikel [ Work with Office Add-ins ][Work with Office Add-ins].

 **Examples:** 

Zeigt, wie man eine Web-Extension zu einem Dokument hinzufügt.

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


[Work with Office Add-ins]: https://docs.aspose.com/words/java/work-with-office-add-ins/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(Object item)](#add-java.lang.Object) |  |
| [clear()](#clear) | Entfernt alle Elemente aus der Sammlung. |
| [get(int index)](#get-int) | Ruft ein Element am angegebenen Index ab. |
| [getCount()](#getCount) | Ermittelt die Anzahl der im Sammelobjekt enthaltenen Elemente. |
| [iterator()](#iterator) | Gibt einen Enumerator zurück, der eine Sammlung durchlaufen kann. |
| [remove(int index)](#remove-int) | Entfernt das Element am angegebenen Index aus der Sammlung. |
| [set(int index, Object value)](#set-int-java.lang.Object) | Setzt ein Element am angegebenen Index. |
### add(Object item) {#add-java.lang.Object}
```
public void add(Object item)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Element | java.lang.Object |  |

### clear() {#clear}
```
public void clear()
```


Entfernt alle Elemente aus der Sammlung.

 **Examples:** 

Zeigt, wie man eine Web-Extension zu einem Dokument hinzufügt.

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

### get(int index) {#get-int}
```
public Object get(int index)
```


Ruft ein Element am angegebenen Index ab.

 **Examples:** 

Zeigt, wie man mit der Sammlung von Web‑Extensions eines Dokuments arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Nullbasierter Index des Elements. |

**Returns:**
java.lang.Object - Ein Element am angegebenen Index.
### getCount() {#getCount}
```
public int getCount()
```


Ermittelt die Anzahl der im Sammelobjekt enthaltenen Elemente.

 **Examples:** 

Zeigt, wie man mit der Sammlung von Web‑Extensions eines Dokuments arbeitet.

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
int – Die Anzahl der im Sammelobjekt enthaltenen Elemente.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt einen Enumerator zurück, der eine Sammlung durchlaufen kann.

 **Examples:** 

Zeigt, wie man mit der Sammlung von Web‑Extensions eines Dokuments arbeitet.

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
### remove(int index) {#remove-int}
```
public void remove(int index)
```


Entfernt das Element am angegebenen Index aus der Sammlung.

 **Examples:** 

Zeigt, wie man mit der Sammlung von Web‑Extensions eines Dokuments arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der nullbasierte Index des Sammlungselements. |

### set(int index, Object value) {#set-int-java.lang.Object}
```
public void set(int index, Object value)
```


Setzt ein Element am angegebenen Index.

 **Examples:** 

Zeigt, wie man mit der Sammlung von Web‑Extensions eines Dokuments arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Nullbasierter Index des Elements. |
| Wert | java.lang.Object | Ein Element am angegebenen Index. |

