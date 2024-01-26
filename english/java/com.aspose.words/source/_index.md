---
title: Source
linktitle: Source
second_title: Aspose.Words for Java
description: Represents an individual source such as a book journal article or interview in Java.
type: docs
weight: 561
url: /java/com.aspose.words/source/
---

**Inheritance:**
java.lang.Object
```
public class Source
```

Represents an individual source, such as a book, journal article, or interview.
## Methods

| Method | Description |
| --- | --- |
| [getAbbreviatedCaseNumber()](#getAbbreviatedCaseNumber) | Gets the abbreviated case number of a source. |
| [getAlbumTitle()](#getAlbumTitle) | Gets the album title of a source. |
| [getBookTitle()](#getBookTitle) | Gets the book title of a source. |
| [getBroadcastTitle()](#getBroadcastTitle) | Gets the broadcast title of a source. |
| [getBroadcaster()](#getBroadcaster) | Gets the broadcaster of a source. |
| [getCaseNumber()](#getCaseNumber) | Gets the case number of a source. |
| [getChapterNumber()](#getChapterNumber) | Gets the chapter number of a source. |
| [getCity()](#getCity) | Gets the city of a source. |
| [getComments()](#getComments) | Gets the comments of a source. |
| [getConferenceName()](#getConferenceName) | Gets the conference or proceedings name of a source. |
| [getContributors()](#getContributors) | Gets contributors list (author, editor, writer etc) of a source. |
| [getCountryOrRegion()](#getCountryOrRegion) | Gets the country or region of a source. |
| [getCourt()](#getCourt) | Gets the court of a source. |
| [getDay()](#getDay) | Gets the day of a source. |
| [getDayAccessed()](#getDayAccessed) | Gets the day accessed of a source. |
| [getDepartment()](#getDepartment) | Gets the department of a source. |
| [getDistributor()](#getDistributor) | Gets the distributor of a source. |
| [getEdition()](#getEdition) | Gets the editor of a source. |
| [getGuid()](#getGuid) | Gets the guid of a source. |
| [getInstitution()](#getInstitution) | Gets the institution of a source. |
| [getInternetSiteTitle()](#getInternetSiteTitle) | Gets the internet site title of a source. |
| [getIssue()](#getIssue) | Gets the issue of a source. |
| [getJournalName()](#getJournalName) | Gets the journal name of a source. |
| [getLcid()](#getLcid) | Gets the locale ID of a source. |
| [getMedium()](#getMedium) | Gets the medium of a source. |
| [getMonth()](#getMonth) | Gets the month of a source. |
| [getMonthAccessed()](#getMonthAccessed) | Gets the month accessed of a source. |
| [getNumberVolumes()](#getNumberVolumes) | Gets the number of volumes of a source. |
| [getPages()](#getPages) | Gets the pages of a source. |
| [getPatentNumber()](#getPatentNumber) | Gets the patent number of a source. |
| [getPeriodicalTitle()](#getPeriodicalTitle) | Gets the periodical title of a source. |
| [getProductionCompany()](#getProductionCompany) | Gets the production company of a source. |
| [getPublicationTitle()](#getPublicationTitle) | Gets the publication title of a source. |
| [getPublisher()](#getPublisher) | Gets the publisher of a source. |
| [getRecordingNumber()](#getRecordingNumber) | Gets the recording number of a source. |
| [getRefOrder()](#getRefOrder) | Gets the reference order of a source. |
| [getReporter()](#getReporter) | Gets the reporter of a source. |
| [getShortTitle()](#getShortTitle) | Gets the short title of a source. |
| [getSourceType()](#getSourceType) | Gets the source type of a source. |
| [getStandardNumber()](#getStandardNumber) | Gets the standard number of a source. |
| [getStateOrProvince()](#getStateOrProvince) | Gets the state or province of a source. |
| [getStation()](#getStation) | Gets the station of a source. |
| [getTag()](#getTag) | Gets the identifying tag name of a source. |
| [getTheater()](#getTheater) | Gets the theater of a source. |
| [getThesisType()](#getThesisType) | Gets the thesis type of a source. |
| [getTitle()](#getTitle) | Gets the title of a source. |
| [getType()](#getType) | Gets the type of a source. |
| [getUrl()](#getUrl) | Gets the url of a source. |
| [getVersion()](#getVersion) | Gets the version of a source. |
| [getVolume()](#getVolume) | Gets the volume of a source. |
| [getYear()](#getYear) | Gets the year of a source. |
| [getYearAccessed()](#getYearAccessed) | Gets the year accessed of a source. |
### getAbbreviatedCaseNumber() {#getAbbreviatedCaseNumber}
```
public String getAbbreviatedCaseNumber()
```


Gets the abbreviated case number of a source.

**Returns:**
java.lang.String - The abbreviated case number of a source.
### getAlbumTitle() {#getAlbumTitle}
```
public String getAlbumTitle()
```


Gets the album title of a source.

**Returns:**
java.lang.String - The album title of a source.
### getBookTitle() {#getBookTitle}
```
public String getBookTitle()
```


Gets the book title of a source.

**Returns:**
java.lang.String - The book title of a source.
### getBroadcastTitle() {#getBroadcastTitle}
```
public String getBroadcastTitle()
```


Gets the broadcast title of a source.

**Returns:**
java.lang.String - The broadcast title of a source.
### getBroadcaster() {#getBroadcaster}
```
public String getBroadcaster()
```


Gets the broadcaster of a source.

**Returns:**
java.lang.String - The broadcaster of a source.
### getCaseNumber() {#getCaseNumber}
```
public String getCaseNumber()
```


Gets the case number of a source.

**Returns:**
java.lang.String - The case number of a source.
### getChapterNumber() {#getChapterNumber}
```
public String getChapterNumber()
```


Gets the chapter number of a source.

**Returns:**
java.lang.String - The chapter number of a source.
### getCity() {#getCity}
```
public String getCity()
```


Gets the city of a source.

**Returns:**
java.lang.String - The city of a source.
### getComments() {#getComments}
```
public String getComments()
```


Gets the comments of a source.

**Returns:**
java.lang.String - The comments of a source.
### getConferenceName() {#getConferenceName}
```
public String getConferenceName()
```


Gets the conference or proceedings name of a source.

**Returns:**
java.lang.String - The conference or proceedings name of a source.
### getContributors() {#getContributors}
```
public ContributorCollection getContributors()
```


Gets contributors list (author, editor, writer etc) of a source.

 **Examples:** 

Shows how to get bibliography sources available in the document.

```

 Document document = new Document(getMyDir() + "Bibliography sources.docx");

 Bibliography bibliography = document.getBibliography();
 Assert.assertEquals(12, bibliography.getSources().size());

 Source source = (Source)bibliography.getSources().toArray()[8];
 Assert.assertEquals(source.getTitle(), "Book 0 (No LCID)");

 ContributorCollection contributors = source.getContributors();
 PersonCollection authors = (PersonCollection)contributors.getAuthor();

 Person person = authors.iterator().next();
 Assert.assertEquals(person.getFirst(), "Roxanne");
 Assert.assertEquals(person.getMiddle(), "Brielle");
 Assert.assertEquals(person.getLast(), "Tejeda");
 
```

**Returns:**
[ContributorCollection](../../com.aspose.words/contributorcollection/) - Contributors list (author, editor, writer etc) of a source.
### getCountryOrRegion() {#getCountryOrRegion}
```
public String getCountryOrRegion()
```


Gets the country or region of a source.

**Returns:**
java.lang.String - The country or region of a source.
### getCourt() {#getCourt}
```
public String getCourt()
```


Gets the court of a source.

**Returns:**
java.lang.String - The court of a source.
### getDay() {#getDay}
```
public String getDay()
```


Gets the day of a source.

**Returns:**
java.lang.String - The day of a source.
### getDayAccessed() {#getDayAccessed}
```
public String getDayAccessed()
```


Gets the day accessed of a source.

**Returns:**
java.lang.String - The day accessed of a source.
### getDepartment() {#getDepartment}
```
public String getDepartment()
```


Gets the department of a source.

**Returns:**
java.lang.String - The department of a source.
### getDistributor() {#getDistributor}
```
public String getDistributor()
```


Gets the distributor of a source.

**Returns:**
java.lang.String - The distributor of a source.
### getEdition() {#getEdition}
```
public String getEdition()
```


Gets the editor of a source.

**Returns:**
java.lang.String - The editor of a source.
### getGuid() {#getGuid}
```
public String getGuid()
```


Gets the guid of a source.

**Returns:**
java.lang.String - The guid of a source.
### getInstitution() {#getInstitution}
```
public String getInstitution()
```


Gets the institution of a source.

**Returns:**
java.lang.String - The institution of a source.
### getInternetSiteTitle() {#getInternetSiteTitle}
```
public String getInternetSiteTitle()
```


Gets the internet site title of a source.

**Returns:**
java.lang.String - The internet site title of a source.
### getIssue() {#getIssue}
```
public String getIssue()
```


Gets the issue of a source.

**Returns:**
java.lang.String - The issue of a source.
### getJournalName() {#getJournalName}
```
public String getJournalName()
```


Gets the journal name of a source.

**Returns:**
java.lang.String - The journal name of a source.
### getLcid() {#getLcid}
```
public String getLcid()
```


Gets the locale ID of a source.

**Returns:**
java.lang.String - The locale ID of a source.
### getMedium() {#getMedium}
```
public String getMedium()
```


Gets the medium of a source.

**Returns:**
java.lang.String - The medium of a source.
### getMonth() {#getMonth}
```
public String getMonth()
```


Gets the month of a source.

**Returns:**
java.lang.String - The month of a source.
### getMonthAccessed() {#getMonthAccessed}
```
public String getMonthAccessed()
```


Gets the month accessed of a source.

**Returns:**
java.lang.String - The month accessed of a source.
### getNumberVolumes() {#getNumberVolumes}
```
public String getNumberVolumes()
```


Gets the number of volumes of a source.

**Returns:**
java.lang.String - The number of volumes of a source.
### getPages() {#getPages}
```
public String getPages()
```


Gets the pages of a source.

**Returns:**
java.lang.String - The pages of a source.
### getPatentNumber() {#getPatentNumber}
```
public String getPatentNumber()
```


Gets the patent number of a source.

**Returns:**
java.lang.String - The patent number of a source.
### getPeriodicalTitle() {#getPeriodicalTitle}
```
public String getPeriodicalTitle()
```


Gets the periodical title of a source.

**Returns:**
java.lang.String - The periodical title of a source.
### getProductionCompany() {#getProductionCompany}
```
public String getProductionCompany()
```


Gets the production company of a source.

**Returns:**
java.lang.String - The production company of a source.
### getPublicationTitle() {#getPublicationTitle}
```
public String getPublicationTitle()
```


Gets the publication title of a source.

**Returns:**
java.lang.String - The publication title of a source.
### getPublisher() {#getPublisher}
```
public String getPublisher()
```


Gets the publisher of a source.

**Returns:**
java.lang.String - The publisher of a source.
### getRecordingNumber() {#getRecordingNumber}
```
public String getRecordingNumber()
```


Gets the recording number of a source.

**Returns:**
java.lang.String - The recording number of a source.
### getRefOrder() {#getRefOrder}
```
public String getRefOrder()
```


Gets the reference order of a source.

**Returns:**
java.lang.String - The reference order of a source.
### getReporter() {#getReporter}
```
public String getReporter()
```


Gets the reporter of a source.

**Returns:**
java.lang.String - The reporter of a source.
### getShortTitle() {#getShortTitle}
```
public String getShortTitle()
```


Gets the short title of a source.

**Returns:**
java.lang.String - The short title of a source.
### getSourceType() {#getSourceType}
```
public int getSourceType()
```


Gets the source type of a source.

**Returns:**
int - The source type of a source. The returned value is one of [SourceType](../../com.aspose.words/sourcetype/) constants.
### getStandardNumber() {#getStandardNumber}
```
public String getStandardNumber()
```


Gets the standard number of a source.

**Returns:**
java.lang.String - The standard number of a source.
### getStateOrProvince() {#getStateOrProvince}
```
public String getStateOrProvince()
```


Gets the state or province of a source.

**Returns:**
java.lang.String - The state or province of a source.
### getStation() {#getStation}
```
public String getStation()
```


Gets the station of a source.

**Returns:**
java.lang.String - The station of a source.
### getTag() {#getTag}
```
public String getTag()
```


Gets the identifying tag name of a source.

**Returns:**
java.lang.String - The identifying tag name of a source.
### getTheater() {#getTheater}
```
public String getTheater()
```


Gets the theater of a source.

**Returns:**
java.lang.String - The theater of a source.
### getThesisType() {#getThesisType}
```
public String getThesisType()
```


Gets the thesis type of a source.

**Returns:**
java.lang.String - The thesis type of a source.
### getTitle() {#getTitle}
```
public String getTitle()
```


Gets the title of a source.

 **Examples:** 

Shows how to get bibliography sources available in the document.

```

 Document document = new Document(getMyDir() + "Bibliography sources.docx");

 Bibliography bibliography = document.getBibliography();
 Assert.assertEquals(12, bibliography.getSources().size());

 Source source = (Source)bibliography.getSources().toArray()[8];
 Assert.assertEquals(source.getTitle(), "Book 0 (No LCID)");

 ContributorCollection contributors = source.getContributors();
 PersonCollection authors = (PersonCollection)contributors.getAuthor();

 Person person = authors.iterator().next();
 Assert.assertEquals(person.getFirst(), "Roxanne");
 Assert.assertEquals(person.getMiddle(), "Brielle");
 Assert.assertEquals(person.getLast(), "Tejeda");
 
```

**Returns:**
java.lang.String - The title of a source.
### getType() {#getType}
```
public String getType()
```


Gets the type of a source.

**Returns:**
java.lang.String - The type of a source.
### getUrl() {#getUrl}
```
public String getUrl()
```


Gets the url of a source.

**Returns:**
java.lang.String - The url of a source.
### getVersion() {#getVersion}
```
public String getVersion()
```


Gets the version of a source.

**Returns:**
java.lang.String - The version of a source.
### getVolume() {#getVolume}
```
public String getVolume()
```


Gets the volume of a source.

**Returns:**
java.lang.String - The volume of a source.
### getYear() {#getYear}
```
public String getYear()
```


Gets the year of a source.

**Returns:**
java.lang.String - The year of a source.
### getYearAccessed() {#getYearAccessed}
```
public String getYearAccessed()
```


Gets the year accessed of a source.

**Returns:**
java.lang.String - The year accessed of a source.
