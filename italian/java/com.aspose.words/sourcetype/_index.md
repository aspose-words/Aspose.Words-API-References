---
title: "SourceType"
linktitle: "SourceType"
second_title: "Aspose.Words per Java"
description: "Rappresenta i tipi di sorgente bibliografica in Java."
type: docs
weight: 627
url: /it/java/com.aspose.words/sourcetype/
---

**Inheritance:**
java.lang.Object
```
public class SourceType
```

Rappresenta i tipi di fonti bibliografiche.

 **Examples:** 

Mostra come ottenere le fonti bibliografiche disponibili nel documento.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [ART](#ART) | Specifica la fonte dell'arte. |
| [ARTICLE_IN_A_PERIODICAL](#ARTICLE-IN-A-PERIODICAL) | Specifica l'articolo in una fonte periodica. |
| [BOOK](#BOOK) | Specifica la fonte del libro. |
| [BOOK_SECTION](#BOOK-SECTION) | Specifica la fonte della sezione del libro. |
| [CASE](#CASE) | Specifica la fonte del caso. |
| [CONFERENCE_PROCEEDINGS](#CONFERENCE-PROCEEDINGS) | Specifica la fonte degli atti della conferenza. |
| [DOCUMENT_FROM_INTERNET_SITE](#DOCUMENT-FROM-INTERNET-SITE) | Specifica il documento dalla fonte del sito internet. |
| [ELECTRONIC](#ELECTRONIC) | Specifica la fonte elettronica. |
| [FILM](#FILM) | Specifica la fonte del film. |
| [INTERNET_SITE](#INTERNET-SITE) | Specifica la fonte del sito internet. |
| [INTERVIEW](#INTERVIEW) | Specifica la fonte dell'intervista. |
| [JOURNAL_ARTICLE](#JOURNAL-ARTICLE) | Specifica la fonte dell'articolo di rivista. |
| [MISC](#MISC) | Specifica la fonte miscellanea. |
| [PATENT](#PATENT) | Specifica la fonte del brevetto. |
| [PERFORMANCE](#PERFORMANCE) | Specifica la fonte della performance. |
| [REPORT](#REPORT) | Specifica la fonte del reporter. |
| [SOUND_RECORDING](#SOUND-RECORDING) | Specifica la fonte della registrazione sonora. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String sourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int sourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sourceType)](#toString-int) |  |
### ART {#ART}
```
public static int ART
```


Specifica la fonte dell'arte.

### ARTICLE_IN_A_PERIODICAL {#ARTICLE-IN-A-PERIODICAL}
```
public static int ARTICLE_IN_A_PERIODICAL
```


Specifica l'articolo in una fonte periodica.

### BOOK {#BOOK}
```
public static int BOOK
```


Specifica la fonte del libro.

### BOOK_SECTION {#BOOK-SECTION}
```
public static int BOOK_SECTION
```


Specifica la fonte della sezione del libro.

### CASE {#CASE}
```
public static int CASE
```


Specifica la fonte del caso.

### CONFERENCE_PROCEEDINGS {#CONFERENCE-PROCEEDINGS}
```
public static int CONFERENCE_PROCEEDINGS
```


Specifica la fonte degli atti della conferenza.

### DOCUMENT_FROM_INTERNET_SITE {#DOCUMENT-FROM-INTERNET-SITE}
```
public static int DOCUMENT_FROM_INTERNET_SITE
```


Specifica il documento dalla fonte del sito internet.

### ELECTRONIC {#ELECTRONIC}
```
public static int ELECTRONIC
```


Specifica la fonte elettronica.

### FILM {#FILM}
```
public static int FILM
```


Specifica la fonte del film.

### INTERNET_SITE {#INTERNET-SITE}
```
public static int INTERNET_SITE
```


Specifica la fonte del sito internet.

### INTERVIEW {#INTERVIEW}
```
public static int INTERVIEW
```


Specifica la fonte dell'intervista.

### JOURNAL_ARTICLE {#JOURNAL-ARTICLE}
```
public static int JOURNAL_ARTICLE
```


Specifica la fonte dell'articolo di rivista.

### MISC {#MISC}
```
public static int MISC
```


Specifica la fonte miscellanea.

### PATENT {#PATENT}
```
public static int PATENT
```


Specifica la fonte del brevetto.

### PERFORMANCE {#PERFORMANCE}
```
public static int PERFORMANCE
```


Specifica la fonte della performance.

### REPORT {#REPORT}
```
public static int REPORT
```


Specifica la fonte del reporter.

### SOUND_RECORDING {#SOUND-RECORDING}
```
public static int SOUND_RECORDING
```


Specifica la fonte della registrazione sonora.

### length {#length}
```
public static int length
```


### fromName(String sourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sourceTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sourceType) {#getName-int}
```
public static String getName(int sourceType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceType | int |  |

**Returns:**
java.lang.String
