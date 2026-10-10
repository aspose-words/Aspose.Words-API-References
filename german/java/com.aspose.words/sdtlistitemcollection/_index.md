---
title: "SdtListItemCollection"
linktitle: "SdtListItemCollection"
second_title: "Aspose.Words für Java"
description: "Stellt Zugriff auf SdtListItem-Elemente eines strukturierten Dokumenten-Tags in Java bereit."
type: docs
weight: 603
url: /de/java/com.aspose.words/sdtlistitemcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class SdtListItemCollection implements Cloneable, Iterable
```

Stellt Zugriff auf [SdtListItem](../../com.aspose.words/sdtlistitem/) Elemente eines strukturierten Dokumenten-Tags bereit.

Weitere Informationen finden Sie im Dokumentationsartikel [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Examples:** 

Zeigt, wie man mit Drop‑Down‑List strukturierten Dokument‑Tags arbeitet.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(SdtListItem item)](#add-com.aspose.words.SdtListItem) | Fügt dieser Sammlung ein Element hinzu. |
| [clear()](#clear) | Löscht alle Elemente aus dieser Sammlung. |
| [get(int index)](#get-int) | Gibt ein [SdtListItem](../../com.aspose.words/sdtlistitem/) Objekt zurück, basierend auf seinem nullbasierten Index in der Sammlung. |
| [getCount()](#getCount) | Ermittelt die Anzahl der Elemente in der Sammlung. |
| [getSelectedValue()](#getSelectedValue) | Gibt den aktuell ausgewählten Wert in dieser Liste an. |
| [iterator()](#iterator) | Gibt ein Iterator-Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [removeAt(int index)](#removeAt-int) | Entfernt ein Listenelement am angegebenen Index. |
| [setSelectedValue(SdtListItem value)](#setSelectedValue-com.aspose.words.SdtListItem) | Gibt den aktuell ausgewählten Wert in dieser Liste an. |
### add(SdtListItem item) {#add-com.aspose.words.SdtListItem}
```
public void add(SdtListItem item)
```


Fügt dieser Sammlung ein Element hinzu.

 **Examples:** 

Zeigt, wie man mit Drop‑Down‑List strukturierten Dokument‑Tags arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| item | [SdtListItem](../../com.aspose.words/sdtlistitem/) |  |

### clear() {#clear}
```
public void clear()
```


Löscht alle Elemente aus dieser Sammlung.

 **Examples:** 

Zeigt, wie man mit Drop‑Down‑List strukturierten Dokument‑Tags arbeitet.

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


Gibt ein [SdtListItem](../../com.aspose.words/sdtlistitem/) Objekt zurück, basierend auf seinem nullbasierten Index in der Sammlung.

 **Examples:** 

Zeigt, wie man mit Drop‑Down‑List strukturierten Dokument‑Tags arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |

**Returns:**
[SdtListItem](../../com.aspose.words/sdtlistitem/) - A [SdtListItem](../../com.aspose.words/sdtlistitem/) object given its zero-based index in the collection.
### getCount() {#getCount}
```
public int getCount()
```


Ermittelt die Anzahl der Elemente in der Sammlung.

 **Examples:** 

Zeigt, wie man mit Drop‑Down‑List strukturierten Dokument‑Tags arbeitet.

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
int - Anzahl der Elemente in der Sammlung.
### getSelectedValue() {#getSelectedValue}
```
public SdtListItem getSelectedValue()
```


Gibt den aktuell ausgewählten Wert in dieser Liste an. Nullwert ist zulässig, was bedeutet, dass kein aktuell ausgewählter Eintrag mit dieser Listenelementsammlung verknüpft ist.

 **Examples:** 

Zeigt, wie man mit Drop‑Down‑List strukturierten Dokument‑Tags arbeitet.

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


Gibt ein Iterator-Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren.

 **Examples:** 

Zeigt, wie man mit Drop‑Down‑List strukturierten Dokument‑Tags arbeitet.

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


Entfernt ein Listenelement am angegebenen Index.

 **Examples:** 

Zeigt, wie man mit Drop‑Down‑List strukturierten Dokument‑Tags arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der nullbasierte Index des zu entfernenden Elements. |

### setSelectedValue(SdtListItem value) {#setSelectedValue-com.aspose.words.SdtListItem}
```
public void setSelectedValue(SdtListItem value)
```


Gibt den aktuell ausgewählten Wert in dieser Liste an. Nullwert ist zulässig, was bedeutet, dass kein aktuell ausgewählter Eintrag mit dieser Listenelementsammlung verknüpft ist.

 **Examples:** 

Zeigt, wie man mit Drop‑Down‑List strukturierten Dokument‑Tags arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [SdtListItem](../../com.aspose.words/sdtlistitem/) | Der entsprechende [SdtListItem](../../com.aspose.words/sdtlistitem/) Wert. |

