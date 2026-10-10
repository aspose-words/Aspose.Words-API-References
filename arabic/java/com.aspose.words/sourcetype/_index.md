---
title: "SourceType"
linktitle: "SourceType"
second_title: "Aspose.Words لـ Java"
description: "يمثل أنواع مصادر الببليوغرافيا في جافا."
type: docs
weight: 627
url: /ar/java/com.aspose.words/sourcetype/
---

**Inheritance:**
java.lang.Object
```
public class SourceType
```

يمثل أنواع مصادر الببليوغرافيا.

 **Examples:** 

يعرض كيفية الحصول على مصادر الببليوغرافيا المتاحة في المستند.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [ART](#ART) | يحدد مصدر الفن. |
| [ARTICLE_IN_A_PERIODICAL](#ARTICLE-IN-A-PERIODICAL) | يحدد المقال في مصدر دوري. |
| [BOOK](#BOOK) | يحدد مصدر الكتاب. |
| [BOOK_SECTION](#BOOK-SECTION) | يحدد مصدر قسم الكتاب. |
| [CASE](#CASE) | يحدد مصدر الحالة. |
| [CONFERENCE_PROCEEDINGS](#CONFERENCE-PROCEEDINGS) | يحدد مصدر وقائع المؤتمر. |
| [DOCUMENT_FROM_INTERNET_SITE](#DOCUMENT-FROM-INTERNET-SITE) | يحدد المستند من مصدر موقع الإنترنت. |
| [ELECTRONIC](#ELECTRONIC) | يحدد المصدر الإلكتروني. |
| [FILM](#FILM) | يحدد مصدر الفيلم. |
| [INTERNET_SITE](#INTERNET-SITE) | يحدد مصدر موقع الإنترنت. |
| [INTERVIEW](#INTERVIEW) | يحدد مصدر المقابلة. |
| [JOURNAL_ARTICLE](#JOURNAL-ARTICLE) | يحدد مصدر مقالة المجلة. |
| [MISC](#MISC) | يحدد المصدر المتنوع. |
| [PATENT](#PATENT) | يحدد مصدر البراءة. |
| [PERFORMANCE](#PERFORMANCE) | يحدد مصدر الأداء. |
| [REPORT](#REPORT) | يحدد مصدر المراسل. |
| [SOUND_RECORDING](#SOUND-RECORDING) | يحدد مصدر التسجيل الصوتي. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String sourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int sourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sourceType)](#toString-int) |  |
### ART {#ART}
```
public static int ART
```


يحدد مصدر الفن.

### ARTICLE_IN_A_PERIODICAL {#ARTICLE-IN-A-PERIODICAL}
```
public static int ARTICLE_IN_A_PERIODICAL
```


يحدد المقال في مصدر دوري.

### BOOK {#BOOK}
```
public static int BOOK
```


يحدد مصدر الكتاب.

### BOOK_SECTION {#BOOK-SECTION}
```
public static int BOOK_SECTION
```


يحدد مصدر قسم الكتاب.

### CASE {#CASE}
```
public static int CASE
```


يحدد مصدر الحالة.

### CONFERENCE_PROCEEDINGS {#CONFERENCE-PROCEEDINGS}
```
public static int CONFERENCE_PROCEEDINGS
```


يحدد مصدر وقائع المؤتمر.

### DOCUMENT_FROM_INTERNET_SITE {#DOCUMENT-FROM-INTERNET-SITE}
```
public static int DOCUMENT_FROM_INTERNET_SITE
```


يحدد المستند من مصدر موقع الإنترنت.

### ELECTRONIC {#ELECTRONIC}
```
public static int ELECTRONIC
```


يحدد المصدر الإلكتروني.

### FILM {#FILM}
```
public static int FILM
```


يحدد مصدر الفيلم.

### INTERNET_SITE {#INTERNET-SITE}
```
public static int INTERNET_SITE
```


يحدد مصدر موقع الإنترنت.

### INTERVIEW {#INTERVIEW}
```
public static int INTERVIEW
```


يحدد مصدر المقابلة.

### JOURNAL_ARTICLE {#JOURNAL-ARTICLE}
```
public static int JOURNAL_ARTICLE
```


يحدد مصدر مقالة المجلة.

### MISC {#MISC}
```
public static int MISC
```


يحدد المصدر المتنوع.

### PATENT {#PATENT}
```
public static int PATENT
```


يحدد مصدر البراءة.

### PERFORMANCE {#PERFORMANCE}
```
public static int PERFORMANCE
```


يحدد مصدر الأداء.

### REPORT {#REPORT}
```
public static int REPORT
```


يحدد مصدر المراسل.

### SOUND_RECORDING {#SOUND-RECORDING}
```
public static int SOUND_RECORDING
```


يحدد مصدر التسجيل الصوتي.

### length {#length}
```
public static int length
```


### fromName(String sourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sourceTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sourceType) {#getName-int}
```
public static String getName(int sourceType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| sourceType | int |  |

**Returns:**
java.lang.String
