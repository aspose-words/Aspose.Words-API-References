---
title: FieldCollection
second_title: Aspose.Words for Java API Reference
description: A collection of  objects that represents the fields in the specified range.
type: docs
weight: 169
url: /java/com.aspose.words/fieldcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class FieldCollection implements Iterable
```

A collection of [Field](../../com.aspose.words/field) objects that represents the fields in the specified range.

To learn more, visit the **Working with Fields** documentation article.

An instance of this collection iterates fields which start fall within the specified range.

The [FieldCollection](../../com.aspose.words/fieldcollection) collection does not own the fields it contains, rather, is just a selection of fields.

The [FieldCollection](../../com.aspose.words/fieldcollection) collection is "live", i.e. changes to the children of the node object that it was created from are immediately reflected in the fields returned by the [FieldCollection](../../com.aspose.words/fieldcollection) properties and methods.
## Methods

| Method | Description |
| --- | --- |
| [getCount()](#getCount--) | Returns the number of the fields in the collection. |
| [get(int index)](#get-int-) | Returns a field at the specified index. |
| [remove(Field field)](#remove-com.aspose.words.Field-) | Removes the specified field from this collection and from the document. |
| [removeAt(int index)](#removeAt-int-) | Removes a field at the specified index from this collection and from the document. |
| [clear()](#clear--) | Removes all fields of this collection from the document and from this collection itself. |
| [iterator()](#iterator--) | Returns an enumerator object. |
### getCount() {#getCount--}
```
public int getCount()
```


Returns the number of the fields in the collection.

**Returns:**
int - The number of the fields in the collection.
### get(int index) {#get-int-}
```
public Field get(int index)
```


Returns a field at the specified index.

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[Field](../../com.aspose.words/field) - A field at the specified index.
### remove(Field field) {#remove-com.aspose.words.Field-}
```
public void remove(Field field)
```


Removes the specified field from this collection and from the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field) | A field to remove. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Removes a field at the specified index from this collection and from the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

### clear() {#clear--}
```
public void clear()
```


Removes all fields of this collection from the document and from this collection itself.

### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an enumerator object.

**Returns:**
java.util.Iterator
