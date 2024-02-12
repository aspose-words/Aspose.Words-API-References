---
title: Person
linktitle: Person
second_title: Aspose.Words for Java
description: Represents individual a person bibliography source contributor in Java.
type: docs
weight: 496
url: /java/com.aspose.words/person/
---

**Inheritance:**
java.lang.Object
```
public class Person
```

Represents individual (a person) bibliography source contributor.

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
| [equals(Object obj)](#equals-java.lang.Object) |  |
| [getFirst()](#getFirst) | Gets the first name of a person. |
| [getLast()](#getLast) | Gets the last name of a person. |
| [getMiddle()](#getMiddle) | Gets the middle name of a person. |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getFirst() {#getFirst}
```
public String getFirst()
```


Gets the first name of a person.

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

**Returns:**
java.lang.String - The first name of a person.
### getLast() {#getLast}
```
public String getLast()
```


Gets the last name of a person.

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

**Returns:**
java.lang.String - The last name of a person.
### getMiddle() {#getMiddle}
```
public String getMiddle()
```


Gets the middle name of a person.

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

**Returns:**
java.lang.String - The middle name of a person.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
