---
title: "SourceType"
linktitle: "SourceType"
second_title: "Aspose.Words для Java"
description: "Представляет типы библиографических источников в Java."
type: docs
weight: 627
url: /ru/java/com.aspose.words/sourcetype/
---

**Inheritance:**
java.lang.Object
```
public class SourceType
```

Представляет типы источников библиографии.

 **Examples:** 

Показывает, как получить доступные в документе источники библиографии.

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
## Поля

| Поле | Описание |
| --- | --- |
| [ART](#ART) | Указывает источник искусства. |
| [ARTICLE_IN_A_PERIODICAL](#ARTICLE-IN-A-PERIODICAL) | Указывает статью в периодическом источнике. |
| [BOOK](#BOOK) | Указывает книжный источник. |
| [BOOK_SECTION](#BOOK-SECTION) | Указывает источник раздела книги. |
| [CASE](#CASE) | Указывает источник судебного дела. |
| [CONFERENCE_PROCEEDINGS](#CONFERENCE-PROCEEDINGS) | Указывает источник материалов конференции. |
| [DOCUMENT_FROM_INTERNET_SITE](#DOCUMENT-FROM-INTERNET-SITE) | Указывает документ из источника интернет‑сайта. |
| [ELECTRONIC](#ELECTRONIC) | Указывает электронный источник. |
| [FILM](#FILM) | Указывает источник фильма. |
| [INTERNET_SITE](#INTERNET-SITE) | Указывает источник интернет‑сайта. |
| [INTERVIEW](#INTERVIEW) | Указывает источник интервью. |
| [JOURNAL_ARTICLE](#JOURNAL-ARTICLE) | Указывает источник статьи в журнале. |
| [MISC](#MISC) | Указывает прочий источник. |
| [PATENT](#PATENT) | Указывает источник патента. |
| [PERFORMANCE](#PERFORMANCE) | Указывает источник выступления. |
| [REPORT](#REPORT) | Указывает источник репортёра. |
| [SOUND_RECORDING](#SOUND-RECORDING) | Указывает источник звуковой записи. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String sourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int sourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sourceType)](#toString-int) |  |
### ART {#ART}
```
public static int ART
```


Указывает источник искусства.

### ARTICLE_IN_A_PERIODICAL {#ARTICLE-IN-A-PERIODICAL}
```
public static int ARTICLE_IN_A_PERIODICAL
```


Указывает статью в периодическом источнике.

### BOOK {#BOOK}
```
public static int BOOK
```


Указывает книжный источник.

### BOOK_SECTION {#BOOK-SECTION}
```
public static int BOOK_SECTION
```


Указывает источник раздела книги.

### CASE {#CASE}
```
public static int CASE
```


Указывает источник судебного дела.

### CONFERENCE_PROCEEDINGS {#CONFERENCE-PROCEEDINGS}
```
public static int CONFERENCE_PROCEEDINGS
```


Указывает источник материалов конференции.

### DOCUMENT_FROM_INTERNET_SITE {#DOCUMENT-FROM-INTERNET-SITE}
```
public static int DOCUMENT_FROM_INTERNET_SITE
```


Указывает документ из источника интернет‑сайта.

### ELECTRONIC {#ELECTRONIC}
```
public static int ELECTRONIC
```


Указывает электронный источник.

### FILM {#FILM}
```
public static int FILM
```


Указывает источник фильма.

### INTERNET_SITE {#INTERNET-SITE}
```
public static int INTERNET_SITE
```


Указывает источник интернет‑сайта.

### INTERVIEW {#INTERVIEW}
```
public static int INTERVIEW
```


Указывает источник интервью.

### JOURNAL_ARTICLE {#JOURNAL-ARTICLE}
```
public static int JOURNAL_ARTICLE
```


Указывает источник статьи в журнале.

### MISC {#MISC}
```
public static int MISC
```


Указывает прочий источник.

### PATENT {#PATENT}
```
public static int PATENT
```


Указывает источник патента.

### PERFORMANCE {#PERFORMANCE}
```
public static int PERFORMANCE
```


Указывает источник выступления.

### REPORT {#REPORT}
```
public static int REPORT
```


Указывает источник репортёра.

### SOUND_RECORDING {#SOUND-RECORDING}
```
public static int SOUND_RECORDING
```


Указывает источник звуковой записи.

### length {#length}
```
public static int length
```


### fromName(String sourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sourceTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sourceType) {#getName-int}
```
public static String getName(int sourceType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceType | int |  |

**Returns:**
java.lang.String
