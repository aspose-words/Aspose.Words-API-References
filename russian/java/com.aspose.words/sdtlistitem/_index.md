---
title: "SdtListItem"
linktitle: "SdtListItem"
second_title: "Aspose.Words для Java"
description: "Этот элемент определяет отдельный элемент списка внутри родительского структурированного тега документа SdtType.COMBO_BOX или SdtType.DROP_DOWN_LIST в Java."
type: docs
weight: 602
url: /ru/java/com.aspose.words/sdtlistitem/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class SdtListItem implements Cloneable
```

Этот элемент определяет отдельный элемент списка внутри родительского структурированного тега документа [SdtType.COMBO\_BOX](../../com.aspose.words/sdttype/\#COMBO-BOX) или [SdtType.DROP\_DOWN\_LIST](../../com.aspose.words/sdttype/\#DROP-DOWN-LIST).

Чтобы узнать больше, посетите статью документации [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Examples:** 

Показывает, как работать со структурированными тегами документа типа выпадающий список.

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
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [SdtListItem(String displayText, String value)](#SdtListItem-java.lang.String-java.lang.String) | Инициализирует новый экземпляр этого класса. |
| [SdtListItem(String value)](#SdtListItem-java.lang.String) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [getDisplayText()](#getDisplayText) | Получает текст, отображаемый в содержимом выполнения вместо содержимого атрибута [getValue()](../../com.aspose.words/sdtlistitem/\#getValue) для этого элемента списка. |
| [getValue()](#getValue) | Получает значение этого элемента списка. |
### SdtListItem(String displayText, String value) {#SdtListItem-java.lang.String-java.lang.String}
```
public SdtListItem(String displayText, String value)
```


Инициализирует новый экземпляр этого класса.

 **Examples:** 

Показывает, как работать со структурированными тегами документа типа выпадающий список.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| displayText | java.lang.String |  |
| значение | java.lang.String |  |

### SdtListItem(String value) {#SdtListItem-java.lang.String}
```
public SdtListItem(String value)
```


Инициализирует новый экземпляр этого класса.

 **Examples:** 

Показывает, как работать со структурированными тегами документа типа выпадающий список.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String |  |

### getDisplayText() {#getDisplayText}
```
public String getDisplayText()
```


Получает текст, отображаемый в содержимом выполнения вместо содержимого атрибута [getValue()](../../com.aspose.words/sdtlistitem/\#getValue) для этого элемента списка.

 **Remarks:** 

Не может быть null и не может быть пустой строкой.

 **Examples:** 

Показывает, как работать со структурированными тегами документа типа выпадающий список.

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
java.lang.String — Текст, отображаемый в содержимом выполнения вместо содержимого атрибута [getValue()](../../com.aspose.words/sdtlistitem/\#getValue) для этого элемента списка.
### getValue() {#getValue}
```
public String getValue()
```


Получает значение этого элемента списка.

 **Remarks:** 

Не может быть null и не может быть пустой строкой.

 **Examples:** 

Показывает, как работать со структурированными тегами документа типа выпадающий список.

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
java.lang.String — Значение этого элемента списка.
