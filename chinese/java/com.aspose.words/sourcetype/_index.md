---
title: "SourceType"
linktitle: "SourceType"
second_title: "Aspose.Words for Java"
description: "表示 Java 中的参考文献来源类型。"
type: docs
weight: 627
url: /zh/java/com.aspose.words/sourcetype/
---

**Inheritance:**
java.lang.Object
```
public class SourceType
```

表示参考文献来源类型。

 **Examples:** 

展示如何获取文档中可用的参考文献来源。

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
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [ART](#ART) | 指定艺术来源。 |
| [ARTICLE_IN_A_PERIODICAL](#ARTICLE-IN-A-PERIODICAL) | 指定期刊来源中的文章。 |
| [BOOK](#BOOK) | 指定图书来源。 |
| [BOOK_SECTION](#BOOK-SECTION) | 指定图书章节来源。 |
| [CASE](#CASE) | 指定案例来源。 |
| [CONFERENCE_PROCEEDINGS](#CONFERENCE-PROCEEDINGS) | 指定会议论文集来源。 |
| [DOCUMENT_FROM_INTERNET_SITE](#DOCUMENT-FROM-INTERNET-SITE) | 指定来自互联网站点的文档来源。 |
| [ELECTRONIC](#ELECTRONIC) | 指定电子来源。 |
| [FILM](#FILM) | 指定影片来源。 |
| [INTERNET_SITE](#INTERNET-SITE) | 指定互联网站点来源。 |
| [INTERVIEW](#INTERVIEW) | 指定访谈来源。 |
| [JOURNAL_ARTICLE](#JOURNAL-ARTICLE) | 指定期刊文章来源。 |
| [MISC](#MISC) | 指定其他来源。 |
| [PATENT](#PATENT) | 指定专利来源。 |
| [PERFORMANCE](#PERFORMANCE) | 指定演出来源。 |
| [REPORT](#REPORT) | 指定记者来源。 |
| [SOUND_RECORDING](#SOUND-RECORDING) | 指定声音录制来源。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String sourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int sourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sourceType)](#toString-int) |  |
### ART {#ART}
```
public static int ART
```


指定艺术来源。

### ARTICLE_IN_A_PERIODICAL {#ARTICLE-IN-A-PERIODICAL}
```
public static int ARTICLE_IN_A_PERIODICAL
```


指定期刊来源中的文章。

### BOOK {#BOOK}
```
public static int BOOK
```


指定图书来源。

### BOOK_SECTION {#BOOK-SECTION}
```
public static int BOOK_SECTION
```


指定图书章节来源。

### CASE {#CASE}
```
public static int CASE
```


指定案例来源。

### CONFERENCE_PROCEEDINGS {#CONFERENCE-PROCEEDINGS}
```
public static int CONFERENCE_PROCEEDINGS
```


指定会议论文集来源。

### DOCUMENT_FROM_INTERNET_SITE {#DOCUMENT-FROM-INTERNET-SITE}
```
public static int DOCUMENT_FROM_INTERNET_SITE
```


指定来自互联网站点的文档来源。

### ELECTRONIC {#ELECTRONIC}
```
public static int ELECTRONIC
```


指定电子来源。

### FILM {#FILM}
```
public static int FILM
```


指定影片来源。

### INTERNET_SITE {#INTERNET-SITE}
```
public static int INTERNET_SITE
```


指定互联网站点来源。

### INTERVIEW {#INTERVIEW}
```
public static int INTERVIEW
```


指定访谈来源。

### JOURNAL_ARTICLE {#JOURNAL-ARTICLE}
```
public static int JOURNAL_ARTICLE
```


指定期刊文章来源。

### MISC {#MISC}
```
public static int MISC
```


指定其他来源。

### PATENT {#PATENT}
```
public static int PATENT
```


指定专利来源。

### PERFORMANCE {#PERFORMANCE}
```
public static int PERFORMANCE
```


指定演出来源。

### REPORT {#REPORT}
```
public static int REPORT
```


指定记者来源。

### SOUND_RECORDING {#SOUND-RECORDING}
```
public static int SOUND_RECORDING
```


指定声音录制来源。

### length {#length}
```
public static int length
```


### fromName(String sourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sourceTypeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sourceType) {#getName-int}
```
public static String getName(int sourceType)
```




**Parameters:**
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceType | int |  |

**Returns:**
java.lang.String
