---
title: Bibliography
linktitle: Bibliography
second_title: Aspose.Words for Java
description: Represents the list of bibliography sources available in the document in Java.
type: docs
weight: 35
url: /java/com.aspose.words/bibliography/
---

**Inheritance:**
java.lang.Object
```
public class Bibliography
```

Represents the list of bibliography sources available in the document.

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
| [getBibliographyStyle()](#getBibliographyStyle) | Gets a string that represents the name of the active style to use for a bibliography. |
| [getSources()](#getSources) | Gets a collection that represents all the sources contained in a bibliography. |
### getBibliographyStyle() {#getBibliographyStyle}
```
public String getBibliographyStyle()
```


Gets a string that represents the name of the active style to use for a bibliography.

**Returns:**
java.lang.String - A string that represents the name of the active style to use for a bibliography.
### getSources() {#getSources}
```
public Collection getSources()
```


Gets a collection that represents all the sources contained in a bibliography.

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
java.util.Collection - A collection that represents all the sources contained in a bibliography.
