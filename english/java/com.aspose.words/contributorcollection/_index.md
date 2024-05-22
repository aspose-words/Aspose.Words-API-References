---
title: ContributorCollection
linktitle: ContributorCollection
second_title: Aspose.Words for Java
description: Represents bibliography source contributors in Java.
type: docs
weight: 117
url: /java/com.aspose.words/contributorcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ContributorCollection implements Iterable
```

Represents bibliography source contributors.

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
| [getArtist()](#getArtist) | Gets the artist of a source. |
| [getAuthor()](#getAuthor) | Gets the author of a source. |
| [getBookAuthor()](#getBookAuthor) | Gets the book author of a source. |
| [getCompiler()](#getCompiler) | Gets the compiler of a source. |
| [getComposer()](#getComposer) | Gets the composer of a source. |
| [getConductor()](#getConductor) | Gets the conductor of a source. |
| [getCounsel()](#getCounsel) | Gets the counsel of a source. |
| [getDirector()](#getDirector) | Gets the director of a source. |
| [getEditor()](#getEditor) | Gets the editor of a source. |
| [getInterviewee()](#getInterviewee) | Gets the interviewee of a source. |
| [getInterviewer()](#getInterviewer) | Gets the interviewer of a source. |
| [getInventor()](#getInventor) | Gets the inventor of a source. |
| [getPerformer()](#getPerformer) | Gets the performer of a source. |
| [getProducer()](#getProducer) | Gets the producer of a source. |
| [getTranslator()](#getTranslator) | Gets the translator of a source. |
| [getWriter()](#getWriter) | Gets the writer of a source. |
| [iterator()](#iterator) |  |
### getArtist() {#getArtist}
```
public Contributor getArtist()
```


Gets the artist of a source.

**Returns:**
[Contributor](../../com.aspose.words/contributor/) - The artist of a source.
### getAuthor() {#getAuthor}
```
public Contributor getAuthor()
```


Gets the author of a source.

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
[Contributor](../../com.aspose.words/contributor/) - The author of a source.
### getBookAuthor() {#getBookAuthor}
```
public Contributor getBookAuthor()
```


Gets the book author of a source.

**Returns:**
[Contributor](../../com.aspose.words/contributor/) - The book author of a source.
### getCompiler() {#getCompiler}
```
public Contributor getCompiler()
```


Gets the compiler of a source.

**Returns:**
[Contributor](../../com.aspose.words/contributor/) - The compiler of a source.
### getComposer() {#getComposer}
```
public Contributor getComposer()
```


Gets the composer of a source.

**Returns:**
[Contributor](../../com.aspose.words/contributor/) - The composer of a source.
### getConductor() {#getConductor}
```
public Contributor getConductor()
```


Gets the conductor of a source.

**Returns:**
[Contributor](../../com.aspose.words/contributor/) - The conductor of a source.
### getCounsel() {#getCounsel}
```
public Contributor getCounsel()
```


Gets the counsel of a source.

**Returns:**
[Contributor](../../com.aspose.words/contributor/) - The counsel of a source.
### getDirector() {#getDirector}
```
public Contributor getDirector()
```


Gets the director of a source.

**Returns:**
[Contributor](../../com.aspose.words/contributor/) - The director of a source.
### getEditor() {#getEditor}
```
public Contributor getEditor()
```


Gets the editor of a source.

**Returns:**
[Contributor](../../com.aspose.words/contributor/) - The editor of a source.
### getInterviewee() {#getInterviewee}
```
public Contributor getInterviewee()
```


Gets the interviewee of a source.

**Returns:**
[Contributor](../../com.aspose.words/contributor/) - The interviewee of a source.
### getInterviewer() {#getInterviewer}
```
public Contributor getInterviewer()
```


Gets the interviewer of a source.

**Returns:**
[Contributor](../../com.aspose.words/contributor/) - The interviewer of a source.
### getInventor() {#getInventor}
```
public Contributor getInventor()
```


Gets the inventor of a source.

**Returns:**
[Contributor](../../com.aspose.words/contributor/) - The inventor of a source.
### getPerformer() {#getPerformer}
```
public Contributor getPerformer()
```


Gets the performer of a source.

**Returns:**
[Contributor](../../com.aspose.words/contributor/) - The performer of a source.
### getProducer() {#getProducer}
```
public Contributor getProducer()
```


Gets the producer of a source.

**Returns:**
[Contributor](../../com.aspose.words/contributor/) - The producer of a source.
### getTranslator() {#getTranslator}
```
public Contributor getTranslator()
```


Gets the translator of a source.

**Returns:**
[Contributor](../../com.aspose.words/contributor/) - The translator of a source.
### getWriter() {#getWriter}
```
public Contributor getWriter()
```


Gets the writer of a source.

**Returns:**
[Contributor](../../com.aspose.words/contributor/) - The writer of a source.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
