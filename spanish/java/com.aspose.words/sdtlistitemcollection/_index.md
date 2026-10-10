---
title: "SdtListItemCollection"
linktitle: "SdtListItemCollection"
second_title: "Aspose.Words para Java"
description: "Proporciona acceso a los elementos SdtListItem de una etiqueta de documento estructurado en Java."
type: docs
weight: 603
url: /es/java/com.aspose.words/sdtlistitemcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class SdtListItemCollection implements Cloneable, Iterable
```

Proporciona acceso a los elementos [SdtListItem](../../com.aspose.words/sdtlistitem/) de una etiqueta de documento estructurado.

Para obtener más información, visite el artículo de documentación [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Examples:** 

Muestra cómo trabajar con etiquetas de documento estructuradas de lista desplegable.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [add(SdtListItem item)](#add-com.aspose.words.SdtListItem) | Agrega un elemento a esta colección. |
| [clear()](#clear) | Elimina todos los elementos de esta colección. |
| [get(int index)](#get-int) | Devuelve un objeto [SdtListItem](../../com.aspose.words/sdtlistitem/) dado su índice basado en cero en la colección. |
| [getCount()](#getCount) | Obtiene el número de elementos en la colección. |
| [getSelectedValue()](#getSelectedValue) | Especifica el valor actualmente seleccionado en esta lista. |
| [iterator()](#iterator) | Devuelve un objeto iterador que puede usarse para iterar sobre todos los elementos de la colección. |
| [removeAt(int index)](#removeAt-int) | Elimina un elemento de la lista en el índice especificado. |
| [setSelectedValue(SdtListItem value)](#setSelectedValue-com.aspose.words.SdtListItem) | Especifica el valor actualmente seleccionado en esta lista. |
### add(SdtListItem item) {#add-com.aspose.words.SdtListItem}
```
public void add(SdtListItem item)
```


Agrega un elemento a esta colección.

 **Examples:** 

Muestra cómo trabajar con etiquetas de documento estructuradas de lista desplegable.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| item | [SdtListItem](../../com.aspose.words/sdtlistitem/) |  |

### clear() {#clear}
```
public void clear()
```


Elimina todos los elementos de esta colección.

 **Examples:** 

Muestra cómo trabajar con etiquetas de documento estructuradas de lista desplegable.

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


Devuelve un objeto [SdtListItem](../../com.aspose.words/sdtlistitem/) dado su índice basado en cero en la colección.

 **Examples:** 

Muestra cómo trabajar con etiquetas de documento estructuradas de lista desplegable.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |

**Returns:**
[SdtListItem](../../com.aspose.words/sdtlistitem/) - A [SdtListItem](../../com.aspose.words/sdtlistitem/) object given its zero-based index in the collection.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de elementos en la colección.

 **Examples:** 

Muestra cómo trabajar con etiquetas de documento estructuradas de lista desplegable.

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
int - Número de elementos en la colección.
### getSelectedValue() {#getSelectedValue}
```
public SdtListItem getSelectedValue()
```


Especifica el valor actualmente seleccionado en esta lista. Se permite un valor nulo, lo que significa que no hay ninguna entrada seleccionada asociada a esta colección de elementos de lista.

 **Examples:** 

Muestra cómo trabajar con etiquetas de documento estructuradas de lista desplegable.

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


Devuelve un objeto iterador que puede usarse para iterar sobre todos los elementos de la colección.

 **Examples:** 

Muestra cómo trabajar con etiquetas de documento estructuradas de lista desplegable.

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


Elimina un elemento de la lista en el índice especificado.

 **Examples:** 

Muestra cómo trabajar con etiquetas de documento estructuradas de lista desplegable.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | El índice basado en cero del elemento a eliminar. |

### setSelectedValue(SdtListItem value) {#setSelectedValue-com.aspose.words.SdtListItem}
```
public void setSelectedValue(SdtListItem value)
```


Especifica el valor actualmente seleccionado en esta lista. Se permite un valor nulo, lo que significa que no hay ninguna entrada seleccionada asociada a esta colección de elementos de lista.

 **Examples:** 

Muestra cómo trabajar con etiquetas de documento estructuradas de lista desplegable.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [SdtListItem](../../com.aspose.words/sdtlistitem/) | El valor correspondiente de [SdtListItem](../../com.aspose.words/sdtlistitem/). |

