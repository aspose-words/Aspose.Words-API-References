---
title: "SourceType"
linktitle: "SourceType"
second_title: "Aspose.Words für Java"
description: "Stellt Bibliographie-Quelltypen in Java dar."
type: docs
weight: 627
url: /de/java/com.aspose.words/sourcetype/
---

**Inheritance:**
java.lang.Object
```
public class SourceType
```

Stellt Bibliographie-Quelltypen dar.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ART](#ART) | Gibt die Kunstquelle an. |
| [ARTICLE_IN_A_PERIODICAL](#ARTICLE-IN-A-PERIODICAL) | Gibt den Artikel in einer Zeitschriftenquelle an. |
| [BOOK](#BOOK) | Gibt die Buchquelle an. |
| [BOOK_SECTION](#BOOK-SECTION) | Gibt die Buchabschnittsquelle an. |
| [CASE](#CASE) | Gibt die Fallquelle an. |
| [CONFERENCE_PROCEEDINGS](#CONFERENCE-PROCEEDINGS) | Gibt die Konferenzbeitragsquelle an. |
| [DOCUMENT_FROM_INTERNET_SITE](#DOCUMENT-FROM-INTERNET-SITE) | Gibt das Dokument aus einer Internetseitenquelle an. |
| [ELECTRONIC](#ELECTRONIC) | Gibt die elektronische Quelle an. |
| [FILM](#FILM) | Gibt die Filmquelle an. |
| [INTERNET_SITE](#INTERNET-SITE) | Gibt die Internetseitenquelle an. |
| [INTERVIEW](#INTERVIEW) | Gibt die Interviewquelle an. |
| [JOURNAL_ARTICLE](#JOURNAL-ARTICLE) | Gibt die Zeitschriftenartikelquelle an. |
| [MISC](#MISC) | Gibt die sonstige Quelle an. |
| [PATENT](#PATENT) | Gibt die Patentquelle an. |
| [PERFORMANCE](#PERFORMANCE) | Gibt die Aufführungsquelle an. |
| [REPORT](#REPORT) | Gibt die Reporterquelle an. |
| [SOUND_RECORDING](#SOUND-RECORDING) | Gibt die Tonaufnahmequelle an. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String sourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int sourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sourceType)](#toString-int) |  |
### ART {#ART}
```
public static int ART
```


Gibt die Kunstquelle an.

### ARTICLE_IN_A_PERIODICAL {#ARTICLE-IN-A-PERIODICAL}
```
public static int ARTICLE_IN_A_PERIODICAL
```


Gibt den Artikel in einer Zeitschriftenquelle an.

### BOOK {#BOOK}
```
public static int BOOK
```


Gibt die Buchquelle an.

### BOOK_SECTION {#BOOK-SECTION}
```
public static int BOOK_SECTION
```


Gibt die Buchabschnittsquelle an.

### CASE {#CASE}
```
public static int CASE
```


Gibt die Fallquelle an.

### CONFERENCE_PROCEEDINGS {#CONFERENCE-PROCEEDINGS}
```
public static int CONFERENCE_PROCEEDINGS
```


Gibt die Konferenzbeitragsquelle an.

### DOCUMENT_FROM_INTERNET_SITE {#DOCUMENT-FROM-INTERNET-SITE}
```
public static int DOCUMENT_FROM_INTERNET_SITE
```


Gibt das Dokument aus einer Internetseitenquelle an.

### ELECTRONIC {#ELECTRONIC}
```
public static int ELECTRONIC
```


Gibt die elektronische Quelle an.

### FILM {#FILM}
```
public static int FILM
```


Gibt die Filmquelle an.

### INTERNET_SITE {#INTERNET-SITE}
```
public static int INTERNET_SITE
```


Gibt die Internetseitenquelle an.

### INTERVIEW {#INTERVIEW}
```
public static int INTERVIEW
```


Gibt die Interviewquelle an.

### JOURNAL_ARTICLE {#JOURNAL-ARTICLE}
```
public static int JOURNAL_ARTICLE
```


Gibt die Zeitschriftenartikelquelle an.

### MISC {#MISC}
```
public static int MISC
```


Gibt die sonstige Quelle an.

### PATENT {#PATENT}
```
public static int PATENT
```


Gibt die Patentquelle an.

### PERFORMANCE {#PERFORMANCE}
```
public static int PERFORMANCE
```


Gibt die Aufführungsquelle an.

### REPORT {#REPORT}
```
public static int REPORT
```


Gibt die Reporterquelle an.

### SOUND_RECORDING {#SOUND-RECORDING}
```
public static int SOUND_RECORDING
```


Gibt die Tonaufnahmequelle an.

### length {#length}
```
public static int length
```


### fromName(String sourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sourceTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sourceType) {#getName-int}
```
public static String getName(int sourceType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceType | int |  |

**Returns:**
java.lang.String
