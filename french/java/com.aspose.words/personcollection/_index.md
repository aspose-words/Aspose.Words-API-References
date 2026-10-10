---
title: "PersonCollection"
linktitle: "PersonCollection"
second_title: "Aspose.Words pour Java"
description: "Représente une liste de personnes qui sont des contributeurs de sources bibliographiques en Java."
type: docs
weight: 546
url: /fr/java/com.aspose.words/personcollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Contributor](../../com.aspose.words/contributor/)

**All Implemented Interfaces:**
java.lang.Iterable
```
public class PersonCollection extends Contributor implements Iterable
```

Représente une liste de personnes qui sont des contributeurs de sources bibliographiques.

 **Examples:** 

Montre comment obtenir les sources bibliographiques disponibles dans le document.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [PersonCollection()](#PersonCollection) | Initialisez une nouvelle instance de la classe [PersonCollection](../../com.aspose.words/personcollection/). |
| [PersonCollection(Iterable persons)](#PersonCollection-java.lang.Iterable) | Initialise une nouvelle instance de cette classe. |
| [PersonCollection(Person[] persons)](#PersonCollection-com.aspose.words.Person...) | Initialisez une nouvelle instance de la classe [PersonCollection](../../com.aspose.words/personcollection/). |
## Méthodes

| Méthode | Description |
| --- | --- |
| [add(Person person)](#add-com.aspose.words.Person) | Ajoute un(e) [Person](../../com.aspose.words/person/) à la collection. |
| [clear()](#clear) | Supprime tous les éléments de la collection. |
| [contains(Person person)](#contains-com.aspose.words.Person) | Détermine si la collection contient une personne spécifique. |
| [get(int index)](#get-int) | Obtient une personne à l'index spécifié. |
| [getCount()](#getCount) | Obtient le nombre de personnes contenues dans la collection. |
| [iterator()](#iterator) |  |
| [remove(Person person)](#remove-com.aspose.words.Person) | Supprime la personne de la collection. |
| [removeAt(int index)](#removeAt-int) | Supprime la personne à l'index spécifié. |
| [set(int index, Person value)](#set-int-com.aspose.words.Person) | Définit une personne à l'index spécifié. |
### PersonCollection() {#PersonCollection}
```
public PersonCollection()
```


Initialisez une nouvelle instance de la classe [PersonCollection](../../com.aspose.words/personcollection/).

 **Examples:** 

Montre comment travailler avec la collection de personnes.

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


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| personnes | java.lang.Iterable |  |

### PersonCollection(Person[] persons) {#PersonCollection-com.aspose.words.Person...}
```
public PersonCollection(Person[] persons)
```


Initialisez une nouvelle instance de la classe [PersonCollection](../../com.aspose.words/personcollection/).

 **Examples:** 

Montre comment travailler avec la collection de personnes.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| persons | [Person\[\]](../../com.aspose.words/person/) |  |

### add(Person person) {#add-com.aspose.words.Person}
```
public void add(Person person)
```


Ajoute un(e) [Person](../../com.aspose.words/person/) à la collection.

 **Examples:** 

Montre comment travailler avec la collection de personnes.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| person | [Person](../../com.aspose.words/person/) | La personne à ajouter à la collection. |

### clear() {#clear}
```
public void clear()
```


Supprime tous les éléments de la collection.

 **Examples:** 

Montre comment travailler avec la collection de personnes.

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


Détermine si la collection contient une personne spécifique.

 **Examples:** 

Montre comment travailler avec la collection de personnes.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| person | [Person](../../com.aspose.words/person/) | La personne à localiser dans la collection. |

**Returns:**
boolean
### get(int index) {#get-int}
```
public Person get(int index)
```


Obtient une personne à l'index spécifié.

 **Examples:** 

Montre comment obtenir les sources bibliographiques disponibles dans le document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | Un index dans la collection. |

**Returns:**
[Person](../../com.aspose.words/person/) - A person at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre de personnes contenues dans la collection.

 **Examples:** 

Montre comment obtenir les sources bibliographiques disponibles dans le document.

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
int - Le nombre de personnes contenues dans la collection.
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


Supprime la personne de la collection.

 **Examples:** 

Montre comment travailler avec la collection de personnes.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| person | [Person](../../com.aspose.words/person/) | La personne à supprimer de la collection. |

**Returns:**
boolean
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Supprime la personne à l'index spécifié.

 **Examples:** 

Montre comment travailler avec la collection de personnes.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index basé sur zéro de la personne à supprimer. |

### set(int index, Person value) {#set-int-com.aspose.words.Person}
```
public void set(int index, Person value)
```


Définit une personne à l'index spécifié.

 **Examples:** 

Montre comment obtenir les sources bibliographiques disponibles dans le document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | Un index dans la collection. |
| value | [Person](../../com.aspose.words/person/) | Une personne à l'index spécifié. |

