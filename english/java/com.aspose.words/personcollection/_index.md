---
title: PersonCollection
linktitle: PersonCollection
second_title: Aspose.Words for Java
description: Represents a list of persons who are bibliography source contributors in Java.
type: docs
weight: 497
url: /java/com.aspose.words/personcollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Contributor](../../com.aspose.words/contributor/)

**All Implemented Interfaces:**
java.lang.Iterable
```
public class PersonCollection extends Contributor implements Iterable
```

Represents a list of persons who are bibliography source contributors.

 **Examples:** 

Shows how to get bibliography sources available in the document.

```

 Document document = new Document(getMyDir() + "Bibliography sources.docx");

 Bibliography bibliography = document.getBibliography();
 Assert.assertEquals(12, bibliography.getSources().size());

 Source source = (Source)bibliography.getSources().toArray()[8];
 Assert.assertEquals(source.getTitle(), "Book 0 (No LCID)");

 ContributorCollection contributors = source.getContributors();
 PersonCollection authors = (PersonCollection)contributors.getAuthor();

 Person person = authors.iterator().next();
 Assert.assertEquals(person.getFirst(), "Roxanne");
 Assert.assertEquals(person.getMiddle(), "Brielle");
 Assert.assertEquals(person.getLast(), "Tejeda");
 
```
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int) | Returns a person at the specified index. |
| [getCount()](#getCount) | Gets the number of elements contained in the collection. |
| [iterator()](#iterator) |  |
### get(int index) {#get-int}
```
public Person get(int index)
```


Returns a person at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[Person](../../com.aspose.words/person/) - A person at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of elements contained in the collection.

**Returns:**
int - The number of elements contained in the collection.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
