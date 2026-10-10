---
title: "PersonCollection"
linktitle: "PersonCollection"
second_title: "Aspose.Words für Java"
description: "Stellt eine Liste von Personen dar, die Bibliografie-Quellbeiträger in Java sind."
type: docs
weight: 546
url: /de/java/com.aspose.words/personcollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Contributor](../../com.aspose.words/contributor/)

**All Implemented Interfaces:**
java.lang.Iterable
```
public class PersonCollection extends Contributor implements Iterable
```

Stellt eine Liste von Personen dar, die Bibliografie‑Quellenbeitragende sind.

 **Examples:** 

Zeigt, wie man die im Dokument verfügbaren Bibliographie‑Quellen abruft.

```

 Document document = new Document(getMyDir() + "Bibliography sources.docx");

 Bibliography bibliography = document.getBibliography();
 Assert.assertEquals(12, bibliography.getSources().size());

 // Get default data from bibliography sources.
 Collection sources = bibliography.getSources();
 Source source = (Source)sources.toArray()[0];
 Assert.assertEquals("Book 0 (No LCID)", source.getTitle());
 Assert.assertEquals(SourceType.BOOK, source.getSourceType());
 Assert.assertNull(source.getAbbreviatedCaseNumber());
 Assert.assertNull(source.getAlbumTitle());
 Assert.assertNull(source.getBookTitle());
 Assert.assertNull(source.getBroadcaster());
 Assert.assertNull(source.getBroadcastTitle());
 Assert.assertNull(source.getCaseNumber());
 Assert.assertNull(source.getChapterNumber());
 Assert.assertNull(source.getComments());
 Assert.assertNull(source.getConferenceName());
 Assert.assertNull(source.getCountryOrRegion());
 Assert.assertNull(source.getCourt());
 Assert.assertNull(source.getDay());
 Assert.assertNull(source.getDayAccessed());
 Assert.assertNull(source.getDepartment());
 Assert.assertNull(source.getDistributor());
 Assert.assertNull(source.getDoi());
 Assert.assertNull(source.getEdition());
 Assert.assertNull(source.getGuid());
 Assert.assertNull(source.getInstitution());
 Assert.assertNull(source.getInternetSiteTitle());
 Assert.assertNull(source.getIssue());
 Assert.assertNull(source.getJournalName());
 Assert.assertNull(source.getLcid());
 Assert.assertNull(source.getMedium());
 Assert.assertNull(source.getMonth());
 Assert.assertNull(source.getMonthAccessed());
 Assert.assertNull(source.getNumberVolumes());
 Assert.assertNull(source.getPages());
 Assert.assertNull(source.getPatentNumber());
 Assert.assertNull(source.getPeriodicalTitle());
 Assert.assertNull(source.getProductionCompany());
 Assert.assertNull(source.getPublicationTitle());
 Assert.assertNull(source.getPublisher());
 Assert.assertNull(source.getRecordingNumber());
 Assert.assertNull(source.getRefOrder());
 Assert.assertNull(source.getReporter());
 Assert.assertNull(source.getShortTitle());
 Assert.assertNull(source.getStandardNumber());
 Assert.assertNull(source.getStateOrProvince());
 Assert.assertNull(source.getStation());
 Assert.assertEquals("BookNoLCID", source.getTag());
 Assert.assertNull(source.getTheater());
 Assert.assertNull(source.getThesisType());
 Assert.assertNull(source.getType());
 Assert.assertNull(source.getUrl());
 Assert.assertNull(source.getVersion());
 Assert.assertNull(source.getVolume());
 Assert.assertNull(source.getYear());
 Assert.assertNull(source.getYearAccessed());

 // Also, you can create a new source.
 Source newSource = new Source("New source", SourceType.MISC);

 ContributorCollection contributors = source.getContributors();
 Assert.assertNull(contributors.getArtist());
 Assert.assertNull(contributors.getBookAuthor());
 Assert.assertNull(contributors.getCompiler());
 Assert.assertNull(contributors.getComposer());
 Assert.assertNull(contributors.getConductor());
 Assert.assertNull(contributors.getCounsel());
 Assert.assertNull(contributors.getDirector());
 Assert.assertNotNull(contributors.getEditor());
 Assert.assertNull(contributors.getInterviewee());
 Assert.assertNull(contributors.getInterviewer());
 Assert.assertNull(contributors.getInventor());
 Assert.assertNull(contributors.getPerformer());
 Assert.assertNull(contributors.getProducer());
 Assert.assertNotNull(contributors.getTranslator());
 Assert.assertNull(contributors.getWriter());

 Contributor editor  = contributors.getEditor();
 Assert.assertEquals(2, ((PersonCollection)editor).getCount());

 PersonCollection authors = (PersonCollection)contributors.getAuthor();
 Assert.assertEquals(2, authors.getCount());

 Person person = authors.get(0);
 Assert.assertEquals("Roxanne", person.getFirst());
 Assert.assertEquals("Brielle", person.getMiddle());
 Assert.assertEquals("Tejeda", person.getLast());
 
```
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [PersonCollection()](#PersonCollection) | Initialisieren Sie eine neue Instanz der Klasse [PersonCollection](../../com.aspose.words/personcollection/). |
| [PersonCollection(Iterable persons)](#PersonCollection-java.lang.Iterable) | Initialisiert eine neue Instanz dieser Klasse. |
| [PersonCollection(Person[] persons)](#PersonCollection-com.aspose.words.Person...) | Initialisieren Sie eine neue Instanz der Klasse [PersonCollection](../../com.aspose.words/personcollection/). |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(Person person)](#add-com.aspose.words.Person) | Fügt der Sammlung ein [Person](../../com.aspose.words/person/) hinzu. |
| [clear()](#clear) | Entfernt alle Elemente aus der Sammlung. |
| [contains(Person person)](#contains-com.aspose.words.Person) | Ermittelt, ob die Sammlung eine bestimmte Person enthält. |
| [get(int index)](#get-int) | Gibt eine Person am angegebenen Index zurück. |
| [getCount()](#getCount) | Gibt die Anzahl der in der Sammlung enthaltenen Personen zurück. |
| [iterator()](#iterator) |  |
| [remove(Person person)](#remove-com.aspose.words.Person) | Entfernt die Person aus der Sammlung. |
| [removeAt(int index)](#removeAt-int) | Entfernt die Person am angegebenen Index. |
| [set(int index, Person value)](#set-int-com.aspose.words.Person) | Setzt eine Person am angegebenen Index. |
### PersonCollection() {#PersonCollection}
```
public PersonCollection()
```


Initialisieren Sie eine neue Instanz der Klasse [PersonCollection](../../com.aspose.words/personcollection/).

 **Examples:** 

Zeigt, wie man mit der Personensammlung arbeitet.

```

 // Create a new person collection.
 PersonCollection persons = new PersonCollection();
 Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
 // Add new person to the collection.
 persons.add(person);
 Assert.assertEquals(1, persons.getCount());
 // Remove person from the collection if it exists.
 if (persons.contains(person))
     persons.remove(person);
 Assert.assertEquals(0, persons.getCount());

 // Create person collection with two persons.
 persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
 Assert.assertEquals(2, persons.getCount());
 // Remove person from the collection by the index.
 persons.removeAt(0);
 Assert.assertEquals(1, persons.getCount());
 // Remove all persons from the collection.
 persons.clear();
 Assert.assertEquals(0, persons.getCount());
 
```

### PersonCollection(Iterable persons) {#PersonCollection-java.lang.Iterable}
```
public PersonCollection(Iterable persons)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Personen | java.lang.Iterable |  |

### PersonCollection(Person[] persons) {#PersonCollection-com.aspose.words.Person...}
```
public PersonCollection(Person[] persons)
```


Initialisieren Sie eine neue Instanz der Klasse [PersonCollection](../../com.aspose.words/personcollection/).

 **Examples:** 

Zeigt, wie man mit der Personensammlung arbeitet.

```

 // Create a new person collection.
 PersonCollection persons = new PersonCollection();
 Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
 // Add new person to the collection.
 persons.add(person);
 Assert.assertEquals(1, persons.getCount());
 // Remove person from the collection if it exists.
 if (persons.contains(person))
     persons.remove(person);
 Assert.assertEquals(0, persons.getCount());

 // Create person collection with two persons.
 persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
 Assert.assertEquals(2, persons.getCount());
 // Remove person from the collection by the index.
 persons.removeAt(0);
 Assert.assertEquals(1, persons.getCount());
 // Remove all persons from the collection.
 persons.clear();
 Assert.assertEquals(0, persons.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| persons | [Person\[\]](../../com.aspose.words/person/) |  |

### add(Person person) {#add-com.aspose.words.Person}
```
public void add(Person person)
```


Fügt der Sammlung ein [Person](../../com.aspose.words/person/) hinzu.

 **Examples:** 

Zeigt, wie man mit der Personensammlung arbeitet.

```

 // Create a new person collection.
 PersonCollection persons = new PersonCollection();
 Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
 // Add new person to the collection.
 persons.add(person);
 Assert.assertEquals(1, persons.getCount());
 // Remove person from the collection if it exists.
 if (persons.contains(person))
     persons.remove(person);
 Assert.assertEquals(0, persons.getCount());

 // Create person collection with two persons.
 persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
 Assert.assertEquals(2, persons.getCount());
 // Remove person from the collection by the index.
 persons.removeAt(0);
 Assert.assertEquals(1, persons.getCount());
 // Remove all persons from the collection.
 persons.clear();
 Assert.assertEquals(0, persons.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| person | [Person](../../com.aspose.words/person/) | Die Person, die zur Sammlung hinzugefügt werden soll. |

### clear() {#clear}
```
public void clear()
```


Entfernt alle Elemente aus der Sammlung.

 **Examples:** 

Zeigt, wie man mit der Personensammlung arbeitet.

```

 // Create a new person collection.
 PersonCollection persons = new PersonCollection();
 Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
 // Add new person to the collection.
 persons.add(person);
 Assert.assertEquals(1, persons.getCount());
 // Remove person from the collection if it exists.
 if (persons.contains(person))
     persons.remove(person);
 Assert.assertEquals(0, persons.getCount());

 // Create person collection with two persons.
 persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
 Assert.assertEquals(2, persons.getCount());
 // Remove person from the collection by the index.
 persons.removeAt(0);
 Assert.assertEquals(1, persons.getCount());
 // Remove all persons from the collection.
 persons.clear();
 Assert.assertEquals(0, persons.getCount());
 
```

### contains(Person person) {#contains-com.aspose.words.Person}
```
public boolean contains(Person person)
```


Ermittelt, ob die Sammlung eine bestimmte Person enthält.

 **Examples:** 

Zeigt, wie man mit der Personensammlung arbeitet.

```

 // Create a new person collection.
 PersonCollection persons = new PersonCollection();
 Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
 // Add new person to the collection.
 persons.add(person);
 Assert.assertEquals(1, persons.getCount());
 // Remove person from the collection if it exists.
 if (persons.contains(person))
     persons.remove(person);
 Assert.assertEquals(0, persons.getCount());

 // Create person collection with two persons.
 persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
 Assert.assertEquals(2, persons.getCount());
 // Remove person from the collection by the index.
 persons.removeAt(0);
 Assert.assertEquals(1, persons.getCount());
 // Remove all persons from the collection.
 persons.clear();
 Assert.assertEquals(0, persons.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| person | [Person](../../com.aspose.words/person/) | Die Person, die in der Sammlung gesucht werden soll. |

**Returns:**
boolean
### get(int index) {#get-int}
```
public Person get(int index)
```


Gibt eine Person am angegebenen Index zurück.

 **Examples:** 

Zeigt, wie man die im Dokument verfügbaren Bibliographie‑Quellen abruft.

```

 Document document = new Document(getMyDir() + "Bibliography sources.docx");

 Bibliography bibliography = document.getBibliography();
 Assert.assertEquals(12, bibliography.getSources().size());

 // Get default data from bibliography sources.
 Collection sources = bibliography.getSources();
 Source source = (Source)sources.toArray()[0];
 Assert.assertEquals("Book 0 (No LCID)", source.getTitle());
 Assert.assertEquals(SourceType.BOOK, source.getSourceType());
 Assert.assertNull(source.getAbbreviatedCaseNumber());
 Assert.assertNull(source.getAlbumTitle());
 Assert.assertNull(source.getBookTitle());
 Assert.assertNull(source.getBroadcaster());
 Assert.assertNull(source.getBroadcastTitle());
 Assert.assertNull(source.getCaseNumber());
 Assert.assertNull(source.getChapterNumber());
 Assert.assertNull(source.getComments());
 Assert.assertNull(source.getConferenceName());
 Assert.assertNull(source.getCountryOrRegion());
 Assert.assertNull(source.getCourt());
 Assert.assertNull(source.getDay());
 Assert.assertNull(source.getDayAccessed());
 Assert.assertNull(source.getDepartment());
 Assert.assertNull(source.getDistributor());
 Assert.assertNull(source.getDoi());
 Assert.assertNull(source.getEdition());
 Assert.assertNull(source.getGuid());
 Assert.assertNull(source.getInstitution());
 Assert.assertNull(source.getInternetSiteTitle());
 Assert.assertNull(source.getIssue());
 Assert.assertNull(source.getJournalName());
 Assert.assertNull(source.getLcid());
 Assert.assertNull(source.getMedium());
 Assert.assertNull(source.getMonth());
 Assert.assertNull(source.getMonthAccessed());
 Assert.assertNull(source.getNumberVolumes());
 Assert.assertNull(source.getPages());
 Assert.assertNull(source.getPatentNumber());
 Assert.assertNull(source.getPeriodicalTitle());
 Assert.assertNull(source.getProductionCompany());
 Assert.assertNull(source.getPublicationTitle());
 Assert.assertNull(source.getPublisher());
 Assert.assertNull(source.getRecordingNumber());
 Assert.assertNull(source.getRefOrder());
 Assert.assertNull(source.getReporter());
 Assert.assertNull(source.getShortTitle());
 Assert.assertNull(source.getStandardNumber());
 Assert.assertNull(source.getStateOrProvince());
 Assert.assertNull(source.getStation());
 Assert.assertEquals("BookNoLCID", source.getTag());
 Assert.assertNull(source.getTheater());
 Assert.assertNull(source.getThesisType());
 Assert.assertNull(source.getType());
 Assert.assertNull(source.getUrl());
 Assert.assertNull(source.getVersion());
 Assert.assertNull(source.getVolume());
 Assert.assertNull(source.getYear());
 Assert.assertNull(source.getYearAccessed());

 // Also, you can create a new source.
 Source newSource = new Source("New source", SourceType.MISC);

 ContributorCollection contributors = source.getContributors();
 Assert.assertNull(contributors.getArtist());
 Assert.assertNull(contributors.getBookAuthor());
 Assert.assertNull(contributors.getCompiler());
 Assert.assertNull(contributors.getComposer());
 Assert.assertNull(contributors.getConductor());
 Assert.assertNull(contributors.getCounsel());
 Assert.assertNull(contributors.getDirector());
 Assert.assertNotNull(contributors.getEditor());
 Assert.assertNull(contributors.getInterviewee());
 Assert.assertNull(contributors.getInterviewer());
 Assert.assertNull(contributors.getInventor());
 Assert.assertNull(contributors.getPerformer());
 Assert.assertNull(contributors.getProducer());
 Assert.assertNotNull(contributors.getTranslator());
 Assert.assertNull(contributors.getWriter());

 Contributor editor  = contributors.getEditor();
 Assert.assertEquals(2, ((PersonCollection)editor).getCount());

 PersonCollection authors = (PersonCollection)contributors.getAuthor();
 Assert.assertEquals(2, authors.getCount());

 Person person = authors.get(0);
 Assert.assertEquals("Roxanne", person.getFirst());
 Assert.assertEquals("Brielle", person.getMiddle());
 Assert.assertEquals("Tejeda", person.getLast());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Ein Index in die Sammlung. |

**Returns:**
[Person](../../com.aspose.words/person/) - A person at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Gibt die Anzahl der in der Sammlung enthaltenen Personen zurück.

 **Examples:** 

Zeigt, wie man die im Dokument verfügbaren Bibliographie‑Quellen abruft.

```

 Document document = new Document(getMyDir() + "Bibliography sources.docx");

 Bibliography bibliography = document.getBibliography();
 Assert.assertEquals(12, bibliography.getSources().size());

 // Get default data from bibliography sources.
 Collection sources = bibliography.getSources();
 Source source = (Source)sources.toArray()[0];
 Assert.assertEquals("Book 0 (No LCID)", source.getTitle());
 Assert.assertEquals(SourceType.BOOK, source.getSourceType());
 Assert.assertNull(source.getAbbreviatedCaseNumber());
 Assert.assertNull(source.getAlbumTitle());
 Assert.assertNull(source.getBookTitle());
 Assert.assertNull(source.getBroadcaster());
 Assert.assertNull(source.getBroadcastTitle());
 Assert.assertNull(source.getCaseNumber());
 Assert.assertNull(source.getChapterNumber());
 Assert.assertNull(source.getComments());
 Assert.assertNull(source.getConferenceName());
 Assert.assertNull(source.getCountryOrRegion());
 Assert.assertNull(source.getCourt());
 Assert.assertNull(source.getDay());
 Assert.assertNull(source.getDayAccessed());
 Assert.assertNull(source.getDepartment());
 Assert.assertNull(source.getDistributor());
 Assert.assertNull(source.getDoi());
 Assert.assertNull(source.getEdition());
 Assert.assertNull(source.getGuid());
 Assert.assertNull(source.getInstitution());
 Assert.assertNull(source.getInternetSiteTitle());
 Assert.assertNull(source.getIssue());
 Assert.assertNull(source.getJournalName());
 Assert.assertNull(source.getLcid());
 Assert.assertNull(source.getMedium());
 Assert.assertNull(source.getMonth());
 Assert.assertNull(source.getMonthAccessed());
 Assert.assertNull(source.getNumberVolumes());
 Assert.assertNull(source.getPages());
 Assert.assertNull(source.getPatentNumber());
 Assert.assertNull(source.getPeriodicalTitle());
 Assert.assertNull(source.getProductionCompany());
 Assert.assertNull(source.getPublicationTitle());
 Assert.assertNull(source.getPublisher());
 Assert.assertNull(source.getRecordingNumber());
 Assert.assertNull(source.getRefOrder());
 Assert.assertNull(source.getReporter());
 Assert.assertNull(source.getShortTitle());
 Assert.assertNull(source.getStandardNumber());
 Assert.assertNull(source.getStateOrProvince());
 Assert.assertNull(source.getStation());
 Assert.assertEquals("BookNoLCID", source.getTag());
 Assert.assertNull(source.getTheater());
 Assert.assertNull(source.getThesisType());
 Assert.assertNull(source.getType());
 Assert.assertNull(source.getUrl());
 Assert.assertNull(source.getVersion());
 Assert.assertNull(source.getVolume());
 Assert.assertNull(source.getYear());
 Assert.assertNull(source.getYearAccessed());

 // Also, you can create a new source.
 Source newSource = new Source("New source", SourceType.MISC);

 ContributorCollection contributors = source.getContributors();
 Assert.assertNull(contributors.getArtist());
 Assert.assertNull(contributors.getBookAuthor());
 Assert.assertNull(contributors.getCompiler());
 Assert.assertNull(contributors.getComposer());
 Assert.assertNull(contributors.getConductor());
 Assert.assertNull(contributors.getCounsel());
 Assert.assertNull(contributors.getDirector());
 Assert.assertNotNull(contributors.getEditor());
 Assert.assertNull(contributors.getInterviewee());
 Assert.assertNull(contributors.getInterviewer());
 Assert.assertNull(contributors.getInventor());
 Assert.assertNull(contributors.getPerformer());
 Assert.assertNull(contributors.getProducer());
 Assert.assertNotNull(contributors.getTranslator());
 Assert.assertNull(contributors.getWriter());

 Contributor editor  = contributors.getEditor();
 Assert.assertEquals(2, ((PersonCollection)editor).getCount());

 PersonCollection authors = (PersonCollection)contributors.getAuthor();
 Assert.assertEquals(2, authors.getCount());

 Person person = authors.get(0);
 Assert.assertEquals("Roxanne", person.getFirst());
 Assert.assertEquals("Brielle", person.getMiddle());
 Assert.assertEquals("Tejeda", person.getLast());
 
```

**Returns:**
int - Die Anzahl der in der Sammlung enthaltenen Personen.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(Person person) {#remove-com.aspose.words.Person}
```
public boolean remove(Person person)
```


Entfernt die Person aus der Sammlung.

 **Examples:** 

Zeigt, wie man mit der Personensammlung arbeitet.

```

 // Create a new person collection.
 PersonCollection persons = new PersonCollection();
 Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
 // Add new person to the collection.
 persons.add(person);
 Assert.assertEquals(1, persons.getCount());
 // Remove person from the collection if it exists.
 if (persons.contains(person))
     persons.remove(person);
 Assert.assertEquals(0, persons.getCount());

 // Create person collection with two persons.
 persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
 Assert.assertEquals(2, persons.getCount());
 // Remove person from the collection by the index.
 persons.removeAt(0);
 Assert.assertEquals(1, persons.getCount());
 // Remove all persons from the collection.
 persons.clear();
 Assert.assertEquals(0, persons.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| person | [Person](../../com.aspose.words/person/) | Die Person, die aus der Sammlung entfernt werden soll. |

**Returns:**
boolean
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Entfernt die Person am angegebenen Index.

 **Examples:** 

Zeigt, wie man mit der Personensammlung arbeitet.

```

 // Create a new person collection.
 PersonCollection persons = new PersonCollection();
 Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
 // Add new person to the collection.
 persons.add(person);
 Assert.assertEquals(1, persons.getCount());
 // Remove person from the collection if it exists.
 if (persons.contains(person))
     persons.remove(person);
 Assert.assertEquals(0, persons.getCount());

 // Create person collection with two persons.
 persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
 Assert.assertEquals(2, persons.getCount());
 // Remove person from the collection by the index.
 persons.removeAt(0);
 Assert.assertEquals(1, persons.getCount());
 // Remove all persons from the collection.
 persons.clear();
 Assert.assertEquals(0, persons.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der nullbasierte Index der zu entfernenden Person. |

### set(int index, Person value) {#set-int-com.aspose.words.Person}
```
public void set(int index, Person value)
```


Setzt eine Person am angegebenen Index.

 **Examples:** 

Zeigt, wie man die im Dokument verfügbaren Bibliographie‑Quellen abruft.

```

 Document document = new Document(getMyDir() + "Bibliography sources.docx");

 Bibliography bibliography = document.getBibliography();
 Assert.assertEquals(12, bibliography.getSources().size());

 // Get default data from bibliography sources.
 Collection sources = bibliography.getSources();
 Source source = (Source)sources.toArray()[0];
 Assert.assertEquals("Book 0 (No LCID)", source.getTitle());
 Assert.assertEquals(SourceType.BOOK, source.getSourceType());
 Assert.assertNull(source.getAbbreviatedCaseNumber());
 Assert.assertNull(source.getAlbumTitle());
 Assert.assertNull(source.getBookTitle());
 Assert.assertNull(source.getBroadcaster());
 Assert.assertNull(source.getBroadcastTitle());
 Assert.assertNull(source.getCaseNumber());
 Assert.assertNull(source.getChapterNumber());
 Assert.assertNull(source.getComments());
 Assert.assertNull(source.getConferenceName());
 Assert.assertNull(source.getCountryOrRegion());
 Assert.assertNull(source.getCourt());
 Assert.assertNull(source.getDay());
 Assert.assertNull(source.getDayAccessed());
 Assert.assertNull(source.getDepartment());
 Assert.assertNull(source.getDistributor());
 Assert.assertNull(source.getDoi());
 Assert.assertNull(source.getEdition());
 Assert.assertNull(source.getGuid());
 Assert.assertNull(source.getInstitution());
 Assert.assertNull(source.getInternetSiteTitle());
 Assert.assertNull(source.getIssue());
 Assert.assertNull(source.getJournalName());
 Assert.assertNull(source.getLcid());
 Assert.assertNull(source.getMedium());
 Assert.assertNull(source.getMonth());
 Assert.assertNull(source.getMonthAccessed());
 Assert.assertNull(source.getNumberVolumes());
 Assert.assertNull(source.getPages());
 Assert.assertNull(source.getPatentNumber());
 Assert.assertNull(source.getPeriodicalTitle());
 Assert.assertNull(source.getProductionCompany());
 Assert.assertNull(source.getPublicationTitle());
 Assert.assertNull(source.getPublisher());
 Assert.assertNull(source.getRecordingNumber());
 Assert.assertNull(source.getRefOrder());
 Assert.assertNull(source.getReporter());
 Assert.assertNull(source.getShortTitle());
 Assert.assertNull(source.getStandardNumber());
 Assert.assertNull(source.getStateOrProvince());
 Assert.assertNull(source.getStation());
 Assert.assertEquals("BookNoLCID", source.getTag());
 Assert.assertNull(source.getTheater());
 Assert.assertNull(source.getThesisType());
 Assert.assertNull(source.getType());
 Assert.assertNull(source.getUrl());
 Assert.assertNull(source.getVersion());
 Assert.assertNull(source.getVolume());
 Assert.assertNull(source.getYear());
 Assert.assertNull(source.getYearAccessed());

 // Also, you can create a new source.
 Source newSource = new Source("New source", SourceType.MISC);

 ContributorCollection contributors = source.getContributors();
 Assert.assertNull(contributors.getArtist());
 Assert.assertNull(contributors.getBookAuthor());
 Assert.assertNull(contributors.getCompiler());
 Assert.assertNull(contributors.getComposer());
 Assert.assertNull(contributors.getConductor());
 Assert.assertNull(contributors.getCounsel());
 Assert.assertNull(contributors.getDirector());
 Assert.assertNotNull(contributors.getEditor());
 Assert.assertNull(contributors.getInterviewee());
 Assert.assertNull(contributors.getInterviewer());
 Assert.assertNull(contributors.getInventor());
 Assert.assertNull(contributors.getPerformer());
 Assert.assertNull(contributors.getProducer());
 Assert.assertNotNull(contributors.getTranslator());
 Assert.assertNull(contributors.getWriter());

 Contributor editor  = contributors.getEditor();
 Assert.assertEquals(2, ((PersonCollection)editor).getCount());

 PersonCollection authors = (PersonCollection)contributors.getAuthor();
 Assert.assertEquals(2, authors.getCount());

 Person person = authors.get(0);
 Assert.assertEquals("Roxanne", person.getFirst());
 Assert.assertEquals("Brielle", person.getMiddle());
 Assert.assertEquals("Tejeda", person.getLast());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Ein Index in die Sammlung. |
| value | [Person](../../com.aspose.words/person/) | Eine Person am angegebenen Index. |

