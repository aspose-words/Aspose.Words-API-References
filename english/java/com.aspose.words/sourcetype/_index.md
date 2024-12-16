---
title: SourceType
linktitle: SourceType
second_title: Aspose.Words for Java
description: Represents bibliography source types in Java.
type: docs
weight: 601
url: /java/com.aspose.words/sourcetype/
---

**Inheritance:**
java.lang.Object
```
public class SourceType
```

Represents bibliography source types.

 **Examples:** 

Shows how to get bibliography sources available in the document.

```

 Document document = new Document(getMyDir() + "Bibliography sources.docx");

 Bibliography bibliography = document.getBibliography();
 Assert.assertEquals(12, bibliography.getSources().size());

 Collection sources = bibliography.getSources();
 Source source = (Source)bibliography.getSources().toArray()[0];
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
## Fields

| Field | Description |
| --- | --- |
| [ART](#ART) | Specifies the art source. |
| [ARTICLE_IN_A_PERIODICAL](#ARTICLE-IN-A-PERIODICAL) | Specifies the article in a periodical source. |
| [BOOK](#BOOK) | Specifies the book source. |
| [BOOK_SECTION](#BOOK-SECTION) | Specifies the book section source. |
| [CASE](#CASE) | Specifies the case source. |
| [CONFERENCE_PROCEEDINGS](#CONFERENCE-PROCEEDINGS) | Specifies the conference proceedings source. |
| [DOCUMENT_FROM_INTERNET_SITE](#DOCUMENT-FROM-INTERNET-SITE) | Specifies the document from internet site source. |
| [ELECTRONIC](#ELECTRONIC) | Specifies the electronic source. |
| [FILM](#FILM) | Specifies the film source. |
| [INTERNET_SITE](#INTERNET-SITE) | Specifies the internet site source. |
| [INTERVIEW](#INTERVIEW) | Specifies the interview source. |
| [JOURNAL_ARTICLE](#JOURNAL-ARTICLE) | Specifies the journal article source. |
| [MISC](#MISC) | Specifies the miscellaneous source. |
| [PATENT](#PATENT) | Specifies the patent source. |
| [PERFORMANCE](#PERFORMANCE) | Specifies the performance source. |
| [REPORT](#REPORT) | Specifies the reporter source. |
| [SOUND_RECORDING](#SOUND-RECORDING) | Specifies the sound recording source. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String sourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int sourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sourceType)](#toString-int) |  |
### ART {#ART}
```
public static int ART
```


Specifies the art source.

### ARTICLE_IN_A_PERIODICAL {#ARTICLE-IN-A-PERIODICAL}
```
public static int ARTICLE_IN_A_PERIODICAL
```


Specifies the article in a periodical source.

### BOOK {#BOOK}
```
public static int BOOK
```


Specifies the book source.

### BOOK_SECTION {#BOOK-SECTION}
```
public static int BOOK_SECTION
```


Specifies the book section source.

### CASE {#CASE}
```
public static int CASE
```


Specifies the case source.

### CONFERENCE_PROCEEDINGS {#CONFERENCE-PROCEEDINGS}
```
public static int CONFERENCE_PROCEEDINGS
```


Specifies the conference proceedings source.

### DOCUMENT_FROM_INTERNET_SITE {#DOCUMENT-FROM-INTERNET-SITE}
```
public static int DOCUMENT_FROM_INTERNET_SITE
```


Specifies the document from internet site source.

### ELECTRONIC {#ELECTRONIC}
```
public static int ELECTRONIC
```


Specifies the electronic source.

### FILM {#FILM}
```
public static int FILM
```


Specifies the film source.

### INTERNET_SITE {#INTERNET-SITE}
```
public static int INTERNET_SITE
```


Specifies the internet site source.

### INTERVIEW {#INTERVIEW}
```
public static int INTERVIEW
```


Specifies the interview source.

### JOURNAL_ARTICLE {#JOURNAL-ARTICLE}
```
public static int JOURNAL_ARTICLE
```


Specifies the journal article source.

### MISC {#MISC}
```
public static int MISC
```


Specifies the miscellaneous source.

### PATENT {#PATENT}
```
public static int PATENT
```


Specifies the patent source.

### PERFORMANCE {#PERFORMANCE}
```
public static int PERFORMANCE
```


Specifies the performance source.

### REPORT {#REPORT}
```
public static int REPORT
```


Specifies the reporter source.

### SOUND_RECORDING {#SOUND-RECORDING}
```
public static int SOUND_RECORDING
```


Specifies the sound recording source.

### length {#length}
```
public static int length
```


### fromName(String sourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sourceTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sourceType) {#getName-int}
```
public static String getName(int sourceType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| sourceType | int |  |

**Returns:**
java.lang.String
