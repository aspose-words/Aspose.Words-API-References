---
title: RevisionGroupCollection
second_title: Aspose.Words for Java API Reference
description: A collection of  objects that represent revision groups in the document.
type: docs
weight: 487
url: /java/com.aspose.words/revisiongroupcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class RevisionGroupCollection implements Iterable
```

A collection of [RevisionGroup](../../com.aspose.words/revisiongroup) objects that represent revision groups in the document.

To learn more, visit the **Track Changes in a Document** documentation article.

You do not create instances of this class directly. Use the [RevisionCollection.getGroups()](../../com.aspose.words/revisioncollection\#getGroups--) property to get revision groups present in a document.
## Methods

| Method | Description |
| --- | --- |
| [iterator()](#iterator--) | Returns an enumerator object. |
| [get(int index)](#get-int-) | Returns a revision group at the specified index. |
| [getCount()](#getCount--) | Returns the number of revision groups in the collection. |
### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an enumerator object.

**Returns:**
java.util.Iterator
### get(int index) {#get-int-}
```
public RevisionGroup get(int index)
```


Returns a revision group at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[RevisionGroup](../../com.aspose.words/revisiongroup) - A revision group at the specified index.
### getCount() {#getCount--}
```
public int getCount()
```


Returns the number of revision groups in the collection.

**Returns:**
int - The number of revision groups in the collection.
