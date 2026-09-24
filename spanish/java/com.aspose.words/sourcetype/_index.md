---
title: "SourceType"
linktitle: "SourceType"
second_title: "Aspose.Words para Java"
description: "Representa los tipos de fuentes bibliográficas en Java."
type: docs
weight: 627
url: /es/java/com.aspose.words/sourcetype/
---

**Inheritance:**
java.lang.Object
```
public class SourceType
```

Representa los tipos de fuentes bibliográficas.

 **Examples:** 

Muestra cómo obtener las fuentes bibliográficas disponibles en el documento.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [ART](#ART) | Especifica la fuente de arte. |
| [ARTICLE_IN_A_PERIODICAL](#ARTICLE-IN-A-PERIODICAL) | Especifica el artículo en una fuente de publicación periódica. |
| [BOOK](#BOOK) | Especifica la fuente del libro. |
| [BOOK_SECTION](#BOOK-SECTION) | Especifica la fuente de la sección del libro. |
| [CASE](#CASE) | Especifica la fuente del caso. |
| [CONFERENCE_PROCEEDINGS](#CONFERENCE-PROCEEDINGS) | Especifica la fuente de los actas de la conferencia. |
| [DOCUMENT_FROM_INTERNET_SITE](#DOCUMENT-FROM-INTERNET-SITE) | Especifica la fuente del documento de un sitio web. |
| [ELECTRONIC](#ELECTRONIC) | Especifica la fuente electrónica. |
| [FILM](#FILM) | Especifica la fuente de la película. |
| [INTERNET_SITE](#INTERNET-SITE) | Especifica la fuente del sitio web. |
| [INTERVIEW](#INTERVIEW) | Especifica la fuente de la entrevista. |
| [JOURNAL_ARTICLE](#JOURNAL-ARTICLE) | Especifica la fuente del artículo de revista. |
| [MISC](#MISC) | Especifica la fuente diversa. |
| [PATENT](#PATENT) | Especifica la fuente de la patente. |
| [PERFORMANCE](#PERFORMANCE) | Especifica la fuente de la actuación. |
| [REPORT](#REPORT) | Especifica la fuente del reportero. |
| [SOUND_RECORDING](#SOUND-RECORDING) | Especifica la fuente de la grabación de sonido. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String sourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int sourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sourceType)](#toString-int) |  |
### ART {#ART}
```
public static int ART
```


Especifica la fuente de arte.

### ARTICLE_IN_A_PERIODICAL {#ARTICLE-IN-A-PERIODICAL}
```
public static int ARTICLE_IN_A_PERIODICAL
```


Especifica el artículo en una fuente de publicación periódica.

### BOOK {#BOOK}
```
public static int BOOK
```


Especifica la fuente del libro.

### BOOK_SECTION {#BOOK-SECTION}
```
public static int BOOK_SECTION
```


Especifica la fuente de la sección del libro.

### CASE {#CASE}
```
public static int CASE
```


Especifica la fuente del caso.

### CONFERENCE_PROCEEDINGS {#CONFERENCE-PROCEEDINGS}
```
public static int CONFERENCE_PROCEEDINGS
```


Especifica la fuente de los actas de la conferencia.

### DOCUMENT_FROM_INTERNET_SITE {#DOCUMENT-FROM-INTERNET-SITE}
```
public static int DOCUMENT_FROM_INTERNET_SITE
```


Especifica la fuente del documento de un sitio web.

### ELECTRONIC {#ELECTRONIC}
```
public static int ELECTRONIC
```


Especifica la fuente electrónica.

### FILM {#FILM}
```
public static int FILM
```


Especifica la fuente de la película.

### INTERNET_SITE {#INTERNET-SITE}
```
public static int INTERNET_SITE
```


Especifica la fuente del sitio web.

### INTERVIEW {#INTERVIEW}
```
public static int INTERVIEW
```


Especifica la fuente de la entrevista.

### JOURNAL_ARTICLE {#JOURNAL-ARTICLE}
```
public static int JOURNAL_ARTICLE
```


Especifica la fuente del artículo de revista.

### MISC {#MISC}
```
public static int MISC
```


Especifica la fuente diversa.

### PATENT {#PATENT}
```
public static int PATENT
```


Especifica la fuente de la patente.

### PERFORMANCE {#PERFORMANCE}
```
public static int PERFORMANCE
```


Especifica la fuente de la actuación.

### REPORT {#REPORT}
```
public static int REPORT
```


Especifica la fuente del reportero.

### SOUND_RECORDING {#SOUND-RECORDING}
```
public static int SOUND_RECORDING
```


Especifica la fuente de la grabación de sonido.

### length {#length}
```
public static int length
```


### fromName(String sourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sourceTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sourceType) {#getName-int}
```
public static String getName(int sourceType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceType | int |  |

**Returns:**
java.lang.String
