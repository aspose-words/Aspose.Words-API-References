---
title: "BaseWebExtensionCollection"
linktitle: "BaseWebExtensionCollection"
second_title: "Aspose.Words Java için"
description: "Java'da TaskPaneCollection, WebExtensionBindingCollection, WebExtensionPropertyCollection ve WebExtensionReferenceCollection koleksiyonları için temel sınıf."
type: docs
weight: 35
url: /tr/java/com.aspose.words/basewebextensioncollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public abstract class BaseWebExtensionCollection implements Iterable
```

Temel sınıf, [TaskPaneCollection](../../com.aspose.words/taskpanecollection/), [WebExtensionBindingCollection](../../com.aspose.words/webextensionbindingcollection/), [WebExtensionPropertyCollection](../../com.aspose.words/webextensionpropertycollection/) ve [WebExtensionReferenceCollection](../../com.aspose.words/webextensionreferencecollection/) koleksiyonları için.

Daha fazla bilgi için, [ Work with Office Add-ins ][Work with Office Add-ins] dokümantasyon makalesini ziyaret edin.


[Work with Office Add-ins]: https://docs.aspose.com/words/java/work-with-office-add-ins/
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [BaseWebExtensionCollection()](#BaseWebExtensionCollection) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [add(Object item)](#add-java.lang.Object) |  |
| [clear()](#clear) | Koleksiyondaki tüm öğeleri kaldırır. |
| [get(int index)](#get-int) | Belirtilen indeksteki öğeyi alır. |
| [getCount()](#getCount) | Koleksiyonda bulunan öğe sayısını alır. |
| [iterator()](#iterator) | Bir koleksiyon içinde yineleyebilen bir enumeratör döndürür. |
| [remove(int index)](#remove-int) | Belirtilen dizindeki öğeyi koleksiyondan kaldırır. |
| [set(int index, Object value)](#set-int-java.lang.Object) | Belirtilen dizinde bir öğe ayarlar. |
### BaseWebExtensionCollection() {#BaseWebExtensionCollection}
```
public BaseWebExtensionCollection()
```


### add(Object item) {#add-java.lang.Object}
```
public void add(Object item)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| öğe | java.lang.Object |  |

### clear() {#clear}
```
public void clear()
```


Koleksiyondaki tüm öğeleri kaldırır.

 **Examples:** 

Bir belgeye web uzantısı eklemenin nasıl yapılacağını gösterir.

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


Belirtilen indeksteki öğeyi alır.

 **Examples:** 

Bir belgenin web uzantıları koleksiyonuyla nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Öğenin sıfır tabanlı indeksi. |

**Returns:**
java.lang.Object - Belirtilen dizindeki bir öğe.
### getCount() {#getCount}
```
public int getCount()
```


Koleksiyonda bulunan öğe sayısını alır.

 **Examples:** 

Bir belgenin web uzantıları koleksiyonuyla nasıl çalışılacağını gösterir.

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
int - Koleksiyonda bulunan öğe sayısı.
### iterator() {#iterator}
```
public Iterator iterator()
```


Bir koleksiyon içinde yineleyebilen bir enumeratör döndürür.

 **Examples:** 

Bir belgenin web uzantıları koleksiyonuyla nasıl çalışılacağını gösterir.

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


Belirtilen dizindeki öğeyi koleksiyondan kaldırır.

 **Examples:** 

Bir belgenin web uzantıları koleksiyonuyla nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Koleksiyon öğesinin sıfır tabanlı indeksi. |

### set(int index, Object value) {#set-int-java.lang.Object}
```
public void set(int index, Object value)
```


Belirtilen dizinde bir öğe ayarlar.

 **Examples:** 

Bir belgenin web uzantıları koleksiyonuyla nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Öğenin sıfır tabanlı indeksi. |
| değer | java.lang.Object | Belirtilen indeksteki bir öğe. |

