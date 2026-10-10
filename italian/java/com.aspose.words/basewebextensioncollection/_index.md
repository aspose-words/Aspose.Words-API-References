---
title: "BaseWebExtensionCollection"
linktitle: "BaseWebExtensionCollection"
second_title: "Aspose.Words per Java"
description: "Classe base per le collezioni TaskPaneCollection, WebExtensionBindingCollection, WebExtensionPropertyCollection e WebExtensionReferenceCollection in Java."
type: docs
weight: 35
url: /it/java/com.aspose.words/basewebextensioncollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public abstract class BaseWebExtensionCollection implements Iterable
```

Classe base per le collezioni [TaskPaneCollection](../../com.aspose.words/taskpanecollection/), [WebExtensionBindingCollection](../../com.aspose.words/webextensionbindingcollection/), [WebExtensionPropertyCollection](../../com.aspose.words/webextensionpropertycollection/) e [WebExtensionReferenceCollection](../../com.aspose.words/webextensionreferencecollection/) collezioni.

Per saperne di più, visita l'articolo di documentazione [ Lavora con gli add-in di Office ][Work with Office Add-ins].


[Work with Office Add-ins]: https://docs.aspose.com/words/java/work-with-office-add-ins/
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [BaseWebExtensionCollection()](#BaseWebExtensionCollection) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [add(Object item)](#add-java.lang.Object) |  |
| [clear()](#clear) | Rimuove tutti gli elementi dalla raccolta. |
| [get(int index)](#get-int) | Ottiene un elemento all'indice specificato. |
| [getCount()](#getCount) | Ottiene il numero di elementi contenuti nella collezione. |
| [iterator()](#iterator) | Restituisce un enumeratore che può iterare attraverso una collezione. |
| [remove(int index)](#remove-int) | Rimuove l'elemento all'indice specificato dalla collezione. |
| [set(int index, Object value)](#set-int-java.lang.Object) | Imposta un elemento all'indice specificato. |
### BaseWebExtensionCollection() {#BaseWebExtensionCollection}
```
public BaseWebExtensionCollection()
```


### add(Object item) {#add-java.lang.Object}
```
public void add(Object item)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| elemento | java.lang.Object |  |

### clear() {#clear}
```
public void clear()
```


Rimuove tutti gli elementi dalla raccolta.

 **Examples:** 

Mostra come aggiungere un'estensione web a un documento.

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


Ottiene un elemento all'indice specificato.

 **Examples:** 

Mostra come lavorare con la collezione di estensioni web di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | Indice basato su zero dell'elemento. |

**Returns:**
java.lang.Object - Un elemento all'indice specificato.
### getCount() {#getCount}
```
public int getCount()
```


Ottiene il numero di elementi contenuti nella collezione.

 **Examples:** 

Mostra come lavorare con la collezione di estensioni web di un documento.

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
int - Il numero di elementi contenuti nella collezione.
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un enumeratore che può iterare attraverso una collezione.

 **Examples:** 

Mostra come lavorare con la collezione di estensioni web di un documento.

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


Rimuove l'elemento all'indice specificato dalla collezione.

 **Examples:** 

Mostra come lavorare con la collezione di estensioni web di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice basato su zero dell'elemento della collezione. |

### set(int index, Object value) {#set-int-java.lang.Object}
```
public void set(int index, Object value)
```


Imposta un elemento all'indice specificato.

 **Examples:** 

Mostra come lavorare con la collezione di estensioni web di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | Indice basato su zero dell'elemento. |
| valore | java.lang.Object | Un elemento all'indice specificato. |

