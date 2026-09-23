---
title: "SdtListItemCollection"
linktitle: "SdtListItemCollection"
second_title: "Aspose.Words per Java"
description: "Fornisce l'accesso agli elementi SdtListItem di un tag di documento strutturato in Java."
type: docs
weight: 603
url: /it/java/com.aspose.words/sdtlistitemcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class SdtListItemCollection implements Cloneable, Iterable
```

Fornisce l'accesso agli elementi [SdtListItem](../../com.aspose.words/sdtlistitem/) di un tag di documento strutturato.

Per saperne di più, visita l'articolo di documentazione [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Examples:** 

Mostra come lavorare con i tag di documento strutturato a elenco a discesa.

```

 Document doc = new Document();
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DROP_DOWN_LIST, MarkupLevel.BLOCK);
 doc.getFirstSection().getBody().appendChild(tag);

 // A drop-down list structured document tag is a form that allows the user to
 // select an option from a list by left-clicking and opening the form in Microsoft Word.
 // The "ListItems" property contains all list items, and each list item is an "SdtListItem".
 SdtListItemCollection listItems = tag.getListItems();
 listItems.add(new SdtListItem("Value 1"));

 Assert.assertEquals(listItems.get(0).getDisplayText(), listItems.get(0).getValue());

 // Add 3 more list items. Initialize these items using a different constructor to the first item
 // to display strings that are different from their values.
 listItems.add(new SdtListItem("Item 2", "Value 2"));
 listItems.add(new SdtListItem("Item 3", "Value 3"));
 listItems.add(new SdtListItem("Item 4", "Value 4"));

 Assert.assertEquals(4, listItems.getCount());

 // The drop-down list is displaying the first item. Assign a different list item to the "SelectedValue" to display it.
 listItems.setSelectedValue(listItems.get(3));

 Assert.assertEquals(listItems.getSelectedValue().getValue(), "Value 4");

 // Enumerate over the collection and print each element.
 Iterator enumerator = listItems.iterator();
 while (enumerator.hasNext()) {
     SdtListItem sdtListItem = enumerator.next();
     System.out.println(MessageFormat.format("List item: {0}, value: {1}", sdtListItem.getDisplayText(), sdtListItem.getValue()));
 }

 // Remove the last list item.
 listItems.removeAt(3);

 Assert.assertEquals(3, listItems.getCount());

 // Since our drop-down control is set to display the removed item by default, give it an item to display which exists.
 listItems.setSelectedValue(listItems.get(1));

 doc.save(getArtifactsDir() + "StructuredDocumentTag.ListItemCollection.docx");

 // Use the "Clear" method to empty the entire drop-down item collection at once.
 listItems.clear();

 Assert.assertEquals(0, listItems.getCount());
 
```


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [add(SdtListItem item)](#add-com.aspose.words.SdtListItem) | Aggiunge un elemento a questa collezione. |
| [clear()](#clear) | Cancella tutti gli elementi da questa collezione. |
| [get(int index)](#get-int) | Restituisce un oggetto [SdtListItem](../../com.aspose.words/sdtlistitem/) dato il suo indice basato su zero nella collezione. |
| [getCount()](#getCount) | Ottiene il numero di elementi nella raccolta. |
| [getSelectedValue()](#getSelectedValue) | Specifica il valore attualmente selezionato in questo elenco. |
| [iterator()](#iterator) | Restituisce un oggetto iteratore che può essere usato per iterare su tutti gli elementi nella collezione. |
| [removeAt(int index)](#removeAt-int) | Rimuove un elemento dell'elenco all'indice specificato. |
| [setSelectedValue(SdtListItem value)](#setSelectedValue-com.aspose.words.SdtListItem) | Specifica il valore attualmente selezionato in questo elenco. |
### add(SdtListItem item) {#add-com.aspose.words.SdtListItem}
```
public void add(SdtListItem item)
```


Aggiunge un elemento a questa collezione.

 **Examples:** 

Mostra come lavorare con i tag di documento strutturato a elenco a discesa.

```

 Document doc = new Document();
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DROP_DOWN_LIST, MarkupLevel.BLOCK);
 doc.getFirstSection().getBody().appendChild(tag);

 // A drop-down list structured document tag is a form that allows the user to
 // select an option from a list by left-clicking and opening the form in Microsoft Word.
 // The "ListItems" property contains all list items, and each list item is an "SdtListItem".
 SdtListItemCollection listItems = tag.getListItems();
 listItems.add(new SdtListItem("Value 1"));

 Assert.assertEquals(listItems.get(0).getDisplayText(), listItems.get(0).getValue());

 // Add 3 more list items. Initialize these items using a different constructor to the first item
 // to display strings that are different from their values.
 listItems.add(new SdtListItem("Item 2", "Value 2"));
 listItems.add(new SdtListItem("Item 3", "Value 3"));
 listItems.add(new SdtListItem("Item 4", "Value 4"));

 Assert.assertEquals(4, listItems.getCount());

 // The drop-down list is displaying the first item. Assign a different list item to the "SelectedValue" to display it.
 listItems.setSelectedValue(listItems.get(3));

 Assert.assertEquals(listItems.getSelectedValue().getValue(), "Value 4");

 // Enumerate over the collection and print each element.
 Iterator enumerator = listItems.iterator();
 while (enumerator.hasNext()) {
     SdtListItem sdtListItem = enumerator.next();
     System.out.println(MessageFormat.format("List item: {0}, value: {1}", sdtListItem.getDisplayText(), sdtListItem.getValue()));
 }

 // Remove the last list item.
 listItems.removeAt(3);

 Assert.assertEquals(3, listItems.getCount());

 // Since our drop-down control is set to display the removed item by default, give it an item to display which exists.
 listItems.setSelectedValue(listItems.get(1));

 doc.save(getArtifactsDir() + "StructuredDocumentTag.ListItemCollection.docx");

 // Use the "Clear" method to empty the entire drop-down item collection at once.
 listItems.clear();

 Assert.assertEquals(0, listItems.getCount());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| item | [SdtListItem](../../com.aspose.words/sdtlistitem/) |  |

### clear() {#clear}
```
public void clear()
```


Cancella tutti gli elementi da questa collezione.

 **Examples:** 

Mostra come lavorare con i tag di documento strutturato a elenco a discesa.

```

 Document doc = new Document();
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DROP_DOWN_LIST, MarkupLevel.BLOCK);
 doc.getFirstSection().getBody().appendChild(tag);

 // A drop-down list structured document tag is a form that allows the user to
 // select an option from a list by left-clicking and opening the form in Microsoft Word.
 // The "ListItems" property contains all list items, and each list item is an "SdtListItem".
 SdtListItemCollection listItems = tag.getListItems();
 listItems.add(new SdtListItem("Value 1"));

 Assert.assertEquals(listItems.get(0).getDisplayText(), listItems.get(0).getValue());

 // Add 3 more list items. Initialize these items using a different constructor to the first item
 // to display strings that are different from their values.
 listItems.add(new SdtListItem("Item 2", "Value 2"));
 listItems.add(new SdtListItem("Item 3", "Value 3"));
 listItems.add(new SdtListItem("Item 4", "Value 4"));

 Assert.assertEquals(4, listItems.getCount());

 // The drop-down list is displaying the first item. Assign a different list item to the "SelectedValue" to display it.
 listItems.setSelectedValue(listItems.get(3));

 Assert.assertEquals(listItems.getSelectedValue().getValue(), "Value 4");

 // Enumerate over the collection and print each element.
 Iterator enumerator = listItems.iterator();
 while (enumerator.hasNext()) {
     SdtListItem sdtListItem = enumerator.next();
     System.out.println(MessageFormat.format("List item: {0}, value: {1}", sdtListItem.getDisplayText(), sdtListItem.getValue()));
 }

 // Remove the last list item.
 listItems.removeAt(3);

 Assert.assertEquals(3, listItems.getCount());

 // Since our drop-down control is set to display the removed item by default, give it an item to display which exists.
 listItems.setSelectedValue(listItems.get(1));

 doc.save(getArtifactsDir() + "StructuredDocumentTag.ListItemCollection.docx");

 // Use the "Clear" method to empty the entire drop-down item collection at once.
 listItems.clear();

 Assert.assertEquals(0, listItems.getCount());
 
```

### get(int index) {#get-int}
```
public SdtListItem get(int index)
```


Restituisce un oggetto [SdtListItem](../../com.aspose.words/sdtlistitem/) dato il suo indice basato su zero nella collezione.

 **Examples:** 

Mostra come lavorare con i tag di documento strutturato a elenco a discesa.

```

 Document doc = new Document();
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DROP_DOWN_LIST, MarkupLevel.BLOCK);
 doc.getFirstSection().getBody().appendChild(tag);

 // A drop-down list structured document tag is a form that allows the user to
 // select an option from a list by left-clicking and opening the form in Microsoft Word.
 // The "ListItems" property contains all list items, and each list item is an "SdtListItem".
 SdtListItemCollection listItems = tag.getListItems();
 listItems.add(new SdtListItem("Value 1"));

 Assert.assertEquals(listItems.get(0).getDisplayText(), listItems.get(0).getValue());

 // Add 3 more list items. Initialize these items using a different constructor to the first item
 // to display strings that are different from their values.
 listItems.add(new SdtListItem("Item 2", "Value 2"));
 listItems.add(new SdtListItem("Item 3", "Value 3"));
 listItems.add(new SdtListItem("Item 4", "Value 4"));

 Assert.assertEquals(4, listItems.getCount());

 // The drop-down list is displaying the first item. Assign a different list item to the "SelectedValue" to display it.
 listItems.setSelectedValue(listItems.get(3));

 Assert.assertEquals(listItems.getSelectedValue().getValue(), "Value 4");

 // Enumerate over the collection and print each element.
 Iterator enumerator = listItems.iterator();
 while (enumerator.hasNext()) {
     SdtListItem sdtListItem = enumerator.next();
     System.out.println(MessageFormat.format("List item: {0}, value: {1}", sdtListItem.getDisplayText(), sdtListItem.getValue()));
 }

 // Remove the last list item.
 listItems.removeAt(3);

 Assert.assertEquals(3, listItems.getCount());

 // Since our drop-down control is set to display the removed item by default, give it an item to display which exists.
 listItems.setSelectedValue(listItems.get(1));

 doc.save(getArtifactsDir() + "StructuredDocumentTag.ListItemCollection.docx");

 // Use the "Clear" method to empty the entire drop-down item collection at once.
 listItems.clear();

 Assert.assertEquals(0, listItems.getCount());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |

**Returns:**
[SdtListItem](../../com.aspose.words/sdtlistitem/) - A [SdtListItem](../../com.aspose.words/sdtlistitem/) object given its zero-based index in the collection.
### getCount() {#getCount}
```
public int getCount()
```


Ottiene il numero di elementi nella raccolta.

 **Examples:** 

Mostra come lavorare con i tag di documento strutturato a elenco a discesa.

```

 Document doc = new Document();
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DROP_DOWN_LIST, MarkupLevel.BLOCK);
 doc.getFirstSection().getBody().appendChild(tag);

 // A drop-down list structured document tag is a form that allows the user to
 // select an option from a list by left-clicking and opening the form in Microsoft Word.
 // The "ListItems" property contains all list items, and each list item is an "SdtListItem".
 SdtListItemCollection listItems = tag.getListItems();
 listItems.add(new SdtListItem("Value 1"));

 Assert.assertEquals(listItems.get(0).getDisplayText(), listItems.get(0).getValue());

 // Add 3 more list items. Initialize these items using a different constructor to the first item
 // to display strings that are different from their values.
 listItems.add(new SdtListItem("Item 2", "Value 2"));
 listItems.add(new SdtListItem("Item 3", "Value 3"));
 listItems.add(new SdtListItem("Item 4", "Value 4"));

 Assert.assertEquals(4, listItems.getCount());

 // The drop-down list is displaying the first item. Assign a different list item to the "SelectedValue" to display it.
 listItems.setSelectedValue(listItems.get(3));

 Assert.assertEquals(listItems.getSelectedValue().getValue(), "Value 4");

 // Enumerate over the collection and print each element.
 Iterator enumerator = listItems.iterator();
 while (enumerator.hasNext()) {
     SdtListItem sdtListItem = enumerator.next();
     System.out.println(MessageFormat.format("List item: {0}, value: {1}", sdtListItem.getDisplayText(), sdtListItem.getValue()));
 }

 // Remove the last list item.
 listItems.removeAt(3);

 Assert.assertEquals(3, listItems.getCount());

 // Since our drop-down control is set to display the removed item by default, give it an item to display which exists.
 listItems.setSelectedValue(listItems.get(1));

 doc.save(getArtifactsDir() + "StructuredDocumentTag.ListItemCollection.docx");

 // Use the "Clear" method to empty the entire drop-down item collection at once.
 listItems.clear();

 Assert.assertEquals(0, listItems.getCount());
 
```

**Returns:**
int - Numero di elementi nella raccolta.
### getSelectedValue() {#getSelectedValue}
```
public SdtListItem getSelectedValue()
```


Specifica il valore attualmente selezionato in questo elenco. È consentito un valore null, il che significa che nessuna voce attualmente selezionata è associata a questa collezione di elementi dell'elenco.

 **Examples:** 

Mostra come lavorare con i tag di documento strutturato a elenco a discesa.

```

 Document doc = new Document();
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DROP_DOWN_LIST, MarkupLevel.BLOCK);
 doc.getFirstSection().getBody().appendChild(tag);

 // A drop-down list structured document tag is a form that allows the user to
 // select an option from a list by left-clicking and opening the form in Microsoft Word.
 // The "ListItems" property contains all list items, and each list item is an "SdtListItem".
 SdtListItemCollection listItems = tag.getListItems();
 listItems.add(new SdtListItem("Value 1"));

 Assert.assertEquals(listItems.get(0).getDisplayText(), listItems.get(0).getValue());

 // Add 3 more list items. Initialize these items using a different constructor to the first item
 // to display strings that are different from their values.
 listItems.add(new SdtListItem("Item 2", "Value 2"));
 listItems.add(new SdtListItem("Item 3", "Value 3"));
 listItems.add(new SdtListItem("Item 4", "Value 4"));

 Assert.assertEquals(4, listItems.getCount());

 // The drop-down list is displaying the first item. Assign a different list item to the "SelectedValue" to display it.
 listItems.setSelectedValue(listItems.get(3));

 Assert.assertEquals(listItems.getSelectedValue().getValue(), "Value 4");

 // Enumerate over the collection and print each element.
 Iterator enumerator = listItems.iterator();
 while (enumerator.hasNext()) {
     SdtListItem sdtListItem = enumerator.next();
     System.out.println(MessageFormat.format("List item: {0}, value: {1}", sdtListItem.getDisplayText(), sdtListItem.getValue()));
 }

 // Remove the last list item.
 listItems.removeAt(3);

 Assert.assertEquals(3, listItems.getCount());

 // Since our drop-down control is set to display the removed item by default, give it an item to display which exists.
 listItems.setSelectedValue(listItems.get(1));

 doc.save(getArtifactsDir() + "StructuredDocumentTag.ListItemCollection.docx");

 // Use the "Clear" method to empty the entire drop-down item collection at once.
 listItems.clear();

 Assert.assertEquals(0, listItems.getCount());
 
```

**Returns:**
[SdtListItem](../../com.aspose.words/sdtlistitem/) - The corresponding [SdtListItem](../../com.aspose.words/sdtlistitem/) value.
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un oggetto iteratore che può essere usato per iterare su tutti gli elementi nella collezione.

 **Examples:** 

Mostra come lavorare con i tag di documento strutturato a elenco a discesa.

```

 Document doc = new Document();
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DROP_DOWN_LIST, MarkupLevel.BLOCK);
 doc.getFirstSection().getBody().appendChild(tag);

 // A drop-down list structured document tag is a form that allows the user to
 // select an option from a list by left-clicking and opening the form in Microsoft Word.
 // The "ListItems" property contains all list items, and each list item is an "SdtListItem".
 SdtListItemCollection listItems = tag.getListItems();
 listItems.add(new SdtListItem("Value 1"));

 Assert.assertEquals(listItems.get(0).getDisplayText(), listItems.get(0).getValue());

 // Add 3 more list items. Initialize these items using a different constructor to the first item
 // to display strings that are different from their values.
 listItems.add(new SdtListItem("Item 2", "Value 2"));
 listItems.add(new SdtListItem("Item 3", "Value 3"));
 listItems.add(new SdtListItem("Item 4", "Value 4"));

 Assert.assertEquals(4, listItems.getCount());

 // The drop-down list is displaying the first item. Assign a different list item to the "SelectedValue" to display it.
 listItems.setSelectedValue(listItems.get(3));

 Assert.assertEquals(listItems.getSelectedValue().getValue(), "Value 4");

 // Enumerate over the collection and print each element.
 Iterator enumerator = listItems.iterator();
 while (enumerator.hasNext()) {
     SdtListItem sdtListItem = enumerator.next();
     System.out.println(MessageFormat.format("List item: {0}, value: {1}", sdtListItem.getDisplayText(), sdtListItem.getValue()));
 }

 // Remove the last list item.
 listItems.removeAt(3);

 Assert.assertEquals(3, listItems.getCount());

 // Since our drop-down control is set to display the removed item by default, give it an item to display which exists.
 listItems.setSelectedValue(listItems.get(1));

 doc.save(getArtifactsDir() + "StructuredDocumentTag.ListItemCollection.docx");

 // Use the "Clear" method to empty the entire drop-down item collection at once.
 listItems.clear();

 Assert.assertEquals(0, listItems.getCount());
 
```

**Returns:**
java.util.Iterator
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Rimuove un elemento dell'elenco all'indice specificato.

 **Examples:** 

Mostra come lavorare con i tag di documento strutturato a elenco a discesa.

```

 Document doc = new Document();
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DROP_DOWN_LIST, MarkupLevel.BLOCK);
 doc.getFirstSection().getBody().appendChild(tag);

 // A drop-down list structured document tag is a form that allows the user to
 // select an option from a list by left-clicking and opening the form in Microsoft Word.
 // The "ListItems" property contains all list items, and each list item is an "SdtListItem".
 SdtListItemCollection listItems = tag.getListItems();
 listItems.add(new SdtListItem("Value 1"));

 Assert.assertEquals(listItems.get(0).getDisplayText(), listItems.get(0).getValue());

 // Add 3 more list items. Initialize these items using a different constructor to the first item
 // to display strings that are different from their values.
 listItems.add(new SdtListItem("Item 2", "Value 2"));
 listItems.add(new SdtListItem("Item 3", "Value 3"));
 listItems.add(new SdtListItem("Item 4", "Value 4"));

 Assert.assertEquals(4, listItems.getCount());

 // The drop-down list is displaying the first item. Assign a different list item to the "SelectedValue" to display it.
 listItems.setSelectedValue(listItems.get(3));

 Assert.assertEquals(listItems.getSelectedValue().getValue(), "Value 4");

 // Enumerate over the collection and print each element.
 Iterator enumerator = listItems.iterator();
 while (enumerator.hasNext()) {
     SdtListItem sdtListItem = enumerator.next();
     System.out.println(MessageFormat.format("List item: {0}, value: {1}", sdtListItem.getDisplayText(), sdtListItem.getValue()));
 }

 // Remove the last list item.
 listItems.removeAt(3);

 Assert.assertEquals(3, listItems.getCount());

 // Since our drop-down control is set to display the removed item by default, give it an item to display which exists.
 listItems.setSelectedValue(listItems.get(1));

 doc.save(getArtifactsDir() + "StructuredDocumentTag.ListItemCollection.docx");

 // Use the "Clear" method to empty the entire drop-down item collection at once.
 listItems.clear();

 Assert.assertEquals(0, listItems.getCount());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice basato su zero dell'elemento da rimuovere. |

### setSelectedValue(SdtListItem value) {#setSelectedValue-com.aspose.words.SdtListItem}
```
public void setSelectedValue(SdtListItem value)
```


Specifica il valore attualmente selezionato in questo elenco. È consentito un valore null, il che significa che nessuna voce attualmente selezionata è associata a questa collezione di elementi dell'elenco.

 **Examples:** 

Mostra come lavorare con i tag di documento strutturato a elenco a discesa.

```

 Document doc = new Document();
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DROP_DOWN_LIST, MarkupLevel.BLOCK);
 doc.getFirstSection().getBody().appendChild(tag);

 // A drop-down list structured document tag is a form that allows the user to
 // select an option from a list by left-clicking and opening the form in Microsoft Word.
 // The "ListItems" property contains all list items, and each list item is an "SdtListItem".
 SdtListItemCollection listItems = tag.getListItems();
 listItems.add(new SdtListItem("Value 1"));

 Assert.assertEquals(listItems.get(0).getDisplayText(), listItems.get(0).getValue());

 // Add 3 more list items. Initialize these items using a different constructor to the first item
 // to display strings that are different from their values.
 listItems.add(new SdtListItem("Item 2", "Value 2"));
 listItems.add(new SdtListItem("Item 3", "Value 3"));
 listItems.add(new SdtListItem("Item 4", "Value 4"));

 Assert.assertEquals(4, listItems.getCount());

 // The drop-down list is displaying the first item. Assign a different list item to the "SelectedValue" to display it.
 listItems.setSelectedValue(listItems.get(3));

 Assert.assertEquals(listItems.getSelectedValue().getValue(), "Value 4");

 // Enumerate over the collection and print each element.
 Iterator enumerator = listItems.iterator();
 while (enumerator.hasNext()) {
     SdtListItem sdtListItem = enumerator.next();
     System.out.println(MessageFormat.format("List item: {0}, value: {1}", sdtListItem.getDisplayText(), sdtListItem.getValue()));
 }

 // Remove the last list item.
 listItems.removeAt(3);

 Assert.assertEquals(3, listItems.getCount());

 // Since our drop-down control is set to display the removed item by default, give it an item to display which exists.
 listItems.setSelectedValue(listItems.get(1));

 doc.save(getArtifactsDir() + "StructuredDocumentTag.ListItemCollection.docx");

 // Use the "Clear" method to empty the entire drop-down item collection at once.
 listItems.clear();

 Assert.assertEquals(0, listItems.getCount());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [SdtListItem](../../com.aspose.words/sdtlistitem/) | Il valore corrispondente di [SdtListItem](../../com.aspose.words/sdtlistitem/). |

