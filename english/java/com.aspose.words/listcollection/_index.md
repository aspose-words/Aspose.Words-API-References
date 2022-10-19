---
title: ListCollection
second_title: Aspose.Words for Java API Reference
description: Stores and manages formatting of bulleted and numbered lists used in a document.
type: docs
weight: 369
url: /java/com.aspose.words/listcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class ListCollection implements Cloneable, Iterable
```

Stores and manages formatting of bulleted and numbered lists used in a document.

To learn more, visit the **Working with Lists** documentation article.

A list in a Microsoft Word document is a set of list formatting properties. The formatting of the lists is stored in the [ListCollection](../../com.aspose.words/listcollection) collection separately from the paragraphs of text.

You do not create objects of this class. There is always only one [ListCollection](../../com.aspose.words/listcollection) object per document and it is accessible via the [DocumentBase.getLists()](../../com.aspose.words/documentbase\#getLists--) property.

To create a new list based on a predefined list template or based on a list style, use the [add(com.aspose.words.Style)](../../com.aspose.words/listcollection\#add-com.aspose.words.Style-) method.

To create a new list with formatting identical to an existing list, use the [addCopy(com.aspose.words.List)](../../com.aspose.words/listcollection\#addCopy-com.aspose.words.List-) method.

To make a paragraph bulleted or numbered, you need to apply list formatting to a paragraph by assigning a [List](../../com.aspose.words/list) object to the [ListFormat.getList()](../../com.aspose.words/listformat\#getList--) / [ListFormat.setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-) property of [ListFormat](../../com.aspose.words/listformat).

To remove list formatting from a paragraph, use the [ListFormat.removeNumbers()](../../com.aspose.words/listformat\#removeNumbers--) method.

If you know a bit about WordprocessingML, then you might know it defines separate concepts for "list" and "list definition". This exactly corresponds to how list formatting is stored in a Microsoft Word document at the low level. List definition is like a "schema" and list is like an instance of a list definition.

To simplify programming model, Aspose.Words hides the distinction between list and list definition in much the same way like Microsoft Word hides this in its user interface. This allows you to concentrate more on how you want your document to look like, rather than building low-level objects to satisfy requirements of the Microsoft Word file format.

It is not possible to delete lists once they are created in the current version of Aspose.Words. This is similar to Microsoft Word where user does not have explicit control over list definitions.
## Methods

| Method | Description |
| --- | --- |
| [iterator()](#iterator--) | Gets the enumerator object that will enumerate lists in the document. |
| [add(int listTemplate)](#add-int-) |  |
| [add(Style listStyle)](#add-com.aspose.words.Style-) | Creates a new list that references a list style and adds it to the collection of lists in the document. |
| [addCopy(List srcList)](#addCopy-com.aspose.words.List-) | Creates a new list by copying the specified list and adding it to the collection of lists in the document. |
| [getListByListId(int listId)](#getListByListId-int-) | Gets a list by a list identifier. |
| [getCount()](#getCount--) | Gets the count of numbered and bulleted lists in the document. |
| [get(int index)](#get-int-) | Gets a list by index. |
| [getDocument()](#getDocument--) | Gets the owner document. |
### iterator() {#iterator--}
```
public Iterator iterator()
```


Gets the enumerator object that will enumerate lists in the document.

**Returns:**
java.util.Iterator
### add(int listTemplate) {#add-int-}
```
public List add(int listTemplate)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
[List](../../com.aspose.words/list)
### add(Style listStyle) {#add-com.aspose.words.Style-}
```
public List add(Style listStyle)
```


Creates a new list that references a list style and adds it to the collection of lists in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| listStyle | [Style](../../com.aspose.words/style) | The list style. |

**Returns:**
[List](../../com.aspose.words/list) - The newly created list.

The newly created list references the list style. If you change the properties of the list style, it is reflected in the properties of the list. Vice versa, if you change the properties of the list, it is reflected in the properties of the list style.
### addCopy(List srcList) {#addCopy-com.aspose.words.List-}
```
public List addCopy(List srcList)
```


Creates a new list by copying the specified list and adding it to the collection of lists in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcList | [List](../../com.aspose.words/list) | The source list to copy from. |

**Returns:**
[List](../../com.aspose.words/list) - The newly created list.

The source list can be from any document. If the source list belongs to a different document, a copy of the list is created and added to the current document.

If the source list is a reference to or a definition of a list style, the newly created list is not related to the original list style.
### getListByListId(int listId) {#getListByListId-int-}
```
public List getListByListId(int listId)
```


Gets a list by a list identifier.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| listId | int | The list identifier. |

**Returns:**
[List](../../com.aspose.words/list) - Returns the list object. Returns null if a list with the specified identifier was not found.

You don't normally need to use this method. Most of the time you apply list formatting to paragraphs just by settings the [ListFormat.getList()](../../com.aspose.words/listformat\#getList--) / [ListFormat.setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-) property of the [ListFormat](../../com.aspose.words/listformat) object.
### getCount() {#getCount--}
```
public int getCount()
```


Gets the count of numbered and bulleted lists in the document.

**Returns:**
int - The count of numbered and bulleted lists in the document.
### get(int index) {#get-int-}
```
public List get(int index)
```


Gets a list by index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[List](../../com.aspose.words/list) - A list by index.
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Gets the owner document.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase) - The owner document.
