---
title: "SourceType"
linktitle: "SourceType"
second_title: "Aspose.Words pour Java"
description: "Représente les types de sources bibliographiques en Java."
type: docs
weight: 627
url: /fr/java/com.aspose.words/sourcetype/
---

**Inheritance:**
java.lang.Object
```
public class SourceType
```

Représente les types de sources bibliographiques.

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
## Champs

| Champ | Description |
| --- | --- |
| [ART](#ART) | Spécifie la source artistique. |
| [ARTICLE_IN_A_PERIODICAL](#ARTICLE-IN-A-PERIODICAL) | Spécifie l'article dans une source périodique. |
| [BOOK](#BOOK) | Spécifie la source du livre. |
| [BOOK_SECTION](#BOOK-SECTION) | Spécifie la source de la section du livre. |
| [CASE](#CASE) | Spécifie la source du cas. |
| [CONFERENCE_PROCEEDINGS](#CONFERENCE-PROCEEDINGS) | Spécifie la source des actes de conférence. |
| [DOCUMENT_FROM_INTERNET_SITE](#DOCUMENT-FROM-INTERNET-SITE) | Spécifie le document provenant d'une source de site Internet. |
| [ELECTRONIC](#ELECTRONIC) | Spécifie la source électronique. |
| [FILM](#FILM) | Spécifie la source du film. |
| [INTERNET_SITE](#INTERNET-SITE) | Spécifie la source du site Internet. |
| [INTERVIEW](#INTERVIEW) | Spécifie la source de l'entretien. |
| [JOURNAL_ARTICLE](#JOURNAL-ARTICLE) | Spécifie la source de l'article de revue. |
| [MISC](#MISC) | Spécifie la source diverse. |
| [PATENT](#PATENT) | Spécifie la source du brevet. |
| [PERFORMANCE](#PERFORMANCE) | Spécifie la source de la performance. |
| [REPORT](#REPORT) | Spécifie la source du reporter. |
| [SOUND_RECORDING](#SOUND-RECORDING) | Spécifie la source de l'enregistrement sonore. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String sourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int sourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sourceType)](#toString-int) |  |
### ART {#ART}
```
public static int ART
```


Spécifie la source artistique.

### ARTICLE_IN_A_PERIODICAL {#ARTICLE-IN-A-PERIODICAL}
```
public static int ARTICLE_IN_A_PERIODICAL
```


Spécifie l'article dans une source périodique.

### BOOK {#BOOK}
```
public static int BOOK
```


Spécifie la source du livre.

### BOOK_SECTION {#BOOK-SECTION}
```
public static int BOOK_SECTION
```


Spécifie la source de la section du livre.

### CASE {#CASE}
```
public static int CASE
```


Spécifie la source du cas.

### CONFERENCE_PROCEEDINGS {#CONFERENCE-PROCEEDINGS}
```
public static int CONFERENCE_PROCEEDINGS
```


Spécifie la source des actes de conférence.

### DOCUMENT_FROM_INTERNET_SITE {#DOCUMENT-FROM-INTERNET-SITE}
```
public static int DOCUMENT_FROM_INTERNET_SITE
```


Spécifie le document provenant d'une source de site Internet.

### ELECTRONIC {#ELECTRONIC}
```
public static int ELECTRONIC
```


Spécifie la source électronique.

### FILM {#FILM}
```
public static int FILM
```


Spécifie la source du film.

### INTERNET_SITE {#INTERNET-SITE}
```
public static int INTERNET_SITE
```


Spécifie la source du site Internet.

### INTERVIEW {#INTERVIEW}
```
public static int INTERVIEW
```


Spécifie la source de l'entretien.

### JOURNAL_ARTICLE {#JOURNAL-ARTICLE}
```
public static int JOURNAL_ARTICLE
```


Spécifie la source de l'article de revue.

### MISC {#MISC}
```
public static int MISC
```


Spécifie la source diverse.

### PATENT {#PATENT}
```
public static int PATENT
```


Spécifie la source du brevet.

### PERFORMANCE {#PERFORMANCE}
```
public static int PERFORMANCE
```


Spécifie la source de la performance.

### REPORT {#REPORT}
```
public static int REPORT
```


Spécifie la source du reporter.

### SOUND_RECORDING {#SOUND-RECORDING}
```
public static int SOUND_RECORDING
```


Spécifie la source de l'enregistrement sonore.

### length {#length}
```
public static int length
```


### fromName(String sourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sourceTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sourceType) {#getName-int}
```
public static String getName(int sourceType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sourceType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sourceType) {#toString-int}
```
public static String toString(int sourceType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sourceType | int |  |

**Returns:**
java.lang.String
