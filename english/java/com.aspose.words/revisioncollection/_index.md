---
title: RevisionCollection
second_title: Aspose.Words for Java API Reference
description: A collection of  objects that represent revisions in the document.
type: docs
weight: 484
url: /java/com.aspose.words/revisioncollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class RevisionCollection implements Iterable
```

A collection of [Revision](../../com.aspose.words/revision) objects that represent revisions in the document.

To learn more, visit the **Track Changes in a Document** documentation article.

You do not create instances of this class directly. Use the [Document.getRevisions()](../../com.aspose.words/document\#getRevisions--) property to get revisions present in a document.
## Methods

| Method | Description |
| --- | --- |
| [acceptAll()](#acceptAll--) | Accepts all revisions in this collection. |
| [rejectAll()](#rejectAll--) | Rejects all revisions in this collection. |
| [getCount()](#getCount--) | Returns the number of revisions in the collection. |
| [get(int index)](#get-int-) | Returns a Revision at the specified index. |
| [getGroups()](#getGroups--) | Collection of revision groups. |
| [iterator()](#iterator--) | Returns an enumerator object. |
### acceptAll() {#acceptAll--}
```
public void acceptAll()
```


Accepts all revisions in this collection.

### rejectAll() {#rejectAll--}
```
public void rejectAll()
```


Rejects all revisions in this collection.

### getCount() {#getCount--}
```
public int getCount()
```


Returns the number of revisions in the collection.

**Returns:**
int - The number of revisions in the collection.
### get(int index) {#get-int-}
```
public Revision get(int index)
```


Returns a Revision at the specified index.

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[Revision](../../com.aspose.words/revision) - A Revision at the specified index.
### getGroups() {#getGroups--}
```
public RevisionGroupCollection getGroups()
```


Collection of revision groups.

**Returns:**
[RevisionGroupCollection](../../com.aspose.words/revisiongroupcollection) - The corresponding [RevisionGroupCollection](../../com.aspose.words/revisiongroupcollection) value.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an enumerator object.

**Returns:**
java.util.Iterator
