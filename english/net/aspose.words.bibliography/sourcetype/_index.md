---
title: SourceType Enum
linktitle: SourceType
articleTitle: SourceType
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Bibliography.SourceType enum for diverse bibliography source types. Enhance your document management with powerful features!
type: docs
weight: 210
url: /net/aspose.words.bibliography/sourcetype/
---
## SourceType enumeration

Represents bibliography source types.

```csharp
public enum SourceType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| ArticleInAPeriodical | `0` | Specifies the article in a periodical source. |
| Book | `1` | Specifies the book source. |
| BookSection | `2` | Specifies the book section source. |
| JournalArticle | `3` | Specifies the journal article source. |
| ConferenceProceedings | `4` | Specifies the conference proceedings source. |
| Report | `5` | Specifies the reporter source. |
| SoundRecording | `6` | Specifies the sound recording source. |
| Performance | `7` | Specifies the performance source. |
| Art | `8` | Specifies the art source. |
| DocumentFromInternetSite | `9` | Specifies the document from internet site source. |
| InternetSite | `10` | Specifies the internet site source. |
| Film | `11` | Specifies the film source. |
| Interview | `12` | Specifies the interview source. |
| Patent | `13` | Specifies the patent source. |
| Electronic | `14` | Specifies the electronic source. |
| Case | `15` | Specifies the case source. |
| Misc | `16` | Specifies the miscellaneous source. |

## Examples

Shows how to get bibliography sources available in the document.

```csharp
Document document = new Document(MyDir + "Bibliography sources.docx");

Bibliography bibliography = document.Bibliography;
Assert.AreEqual(12, bibliography.Sources.Count);

// Get default data from bibliography sources.
Source source = bibliography.Sources.FirstOrDefault();
Assert.AreEqual("Book 0 (No LCID)", source.Title);
Assert.AreEqual(SourceType.Book, source.SourceType);
Assert.AreEqual(3, source.Contributors.Count());
Assert.IsNull(source.AbbreviatedCaseNumber);
Assert.IsNull(source.AlbumTitle);
Assert.IsNull(source.BookTitle);
Assert.IsNull(source.Broadcaster);
Assert.IsNull(source.BroadcastTitle);
Assert.IsNull(source.CaseNumber);
Assert.IsNull(source.ChapterNumber);
Assert.IsNull(source.Comments);
Assert.IsNull(source.ConferenceName);
Assert.IsNull(source.CountryOrRegion);
Assert.IsNull(source.Court);
Assert.IsNull(source.Day);
Assert.IsNull(source.DayAccessed);
Assert.IsNull(source.Department);
Assert.IsNull(source.Distributor);
Assert.IsNull(source.Doi);
Assert.IsNull(source.Edition);
Assert.IsNull(source.Guid);
Assert.IsNull(source.Institution);
Assert.IsNull(source.InternetSiteTitle);
Assert.IsNull(source.Issue);
Assert.IsNull(source.JournalName);
Assert.IsNull(source.Lcid);
Assert.IsNull(source.Medium);
Assert.IsNull(source.Month);
Assert.IsNull(source.MonthAccessed);
Assert.IsNull(source.NumberVolumes);
Assert.IsNull(source.Pages);
Assert.IsNull(source.PatentNumber);
Assert.IsNull(source.PeriodicalTitle);
Assert.IsNull(source.ProductionCompany);
Assert.IsNull(source.PublicationTitle);
Assert.IsNull(source.Publisher);
Assert.IsNull(source.RecordingNumber);
Assert.IsNull(source.RefOrder);
Assert.IsNull(source.Reporter);
Assert.IsNull(source.ShortTitle);
Assert.IsNull(source.StandardNumber);
Assert.IsNull(source.StateOrProvince);
Assert.IsNull(source.Station);
Assert.AreEqual("BookNoLCID", source.Tag);
Assert.IsNull(source.Theater);
Assert.IsNull(source.ThesisType);
Assert.IsNull(source.Type);
Assert.IsNull(source.Url);
Assert.IsNull(source.Version);
Assert.IsNull(source.Volume);
Assert.IsNull(source.Year);
Assert.IsNull(source.YearAccessed);

// Also, you can create a new source.
Source newSource = new Source("New source", SourceType.Misc);

ContributorCollection contributors = source.Contributors;
Assert.IsNull(contributors.Artist);
Assert.IsNull(contributors.BookAuthor);
Assert.IsNull(contributors.Compiler);
Assert.IsNull(contributors.Composer);
Assert.IsNull(contributors.Conductor);
Assert.IsNull(contributors.Counsel);
Assert.IsNull(contributors.Director);
Assert.IsNotNull(contributors.Editor);
Assert.IsNull(contributors.Interviewee);
Assert.IsNull(contributors.Interviewer);
Assert.IsNull(contributors.Inventor);
Assert.IsNull(contributors.Performer);
Assert.IsNull(contributors.Producer);
Assert.IsNotNull(contributors.Translator);
Assert.IsNull(contributors.Writer);

Contributor editor  = contributors.Editor;
Assert.AreEqual(2, ((PersonCollection)editor).Count());

PersonCollection authors = (PersonCollection)contributors.Author;
Assert.AreEqual(2, authors.Count());

Person person = authors[0];
Assert.AreEqual("Roxanne", person.First);
Assert.AreEqual("Brielle", person.Middle);
Assert.AreEqual("Tejeda", person.Last);
```

### See Also

* namespace [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* assembly [Aspose.Words](../../)
