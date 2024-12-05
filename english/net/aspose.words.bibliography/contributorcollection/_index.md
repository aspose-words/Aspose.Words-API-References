---
title: ContributorCollection Class
linktitle: ContributorCollection
articleTitle: ContributorCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Bibliography.ContributorCollection class. Represents bibliography source contributors in C#.
type: docs
weight: 140
url: /net/aspose.words.bibliography/contributorcollection/
---
## ContributorCollection class

Represents bibliography source contributors.

```csharp
public sealed class ContributorCollection : IEnumerable<Contributor>
```

## Properties

| Name | Description |
| --- | --- |
| [Artist](../../aspose.words.bibliography/contributorcollection/artist/) { get; set; } | Gets or sets the artist of a source. |
| [Author](../../aspose.words.bibliography/contributorcollection/author/) { get; set; } | Gets or sets the author of a source. |
| [BookAuthor](../../aspose.words.bibliography/contributorcollection/bookauthor/) { get; set; } | Gets or sets the book author of a source. |
| [Compiler](../../aspose.words.bibliography/contributorcollection/compiler/) { get; set; } | Gets or sets the compiler of a source. |
| [Composer](../../aspose.words.bibliography/contributorcollection/composer/) { get; set; } | Gets or sets the composer of a source. |
| [Conductor](../../aspose.words.bibliography/contributorcollection/conductor/) { get; set; } | Gets or sets the conductor of a source. |
| [Counsel](../../aspose.words.bibliography/contributorcollection/counsel/) { get; set; } | Gets or sets the counsel of a source. |
| [Director](../../aspose.words.bibliography/contributorcollection/director/) { get; set; } | Gets or sets the director of a source. |
| [Editor](../../aspose.words.bibliography/contributorcollection/editor/) { get; set; } | Gets or sets the editor of a source. |
| [Interviewee](../../aspose.words.bibliography/contributorcollection/interviewee/) { get; set; } | Gets or sets the interviewee of a source. |
| [Interviewer](../../aspose.words.bibliography/contributorcollection/interviewer/) { get; set; } | Gets or sets the interviewer of a source. |
| [Inventor](../../aspose.words.bibliography/contributorcollection/inventor/) { get; set; } | Gets or sets the inventor of a source. |
| [Performer](../../aspose.words.bibliography/contributorcollection/performer/) { get; set; } | Gets or sets the performer of a source. |
| [Producer](../../aspose.words.bibliography/contributorcollection/producer/) { get; set; } | Gets or sets the producer of a source. |
| [Translator](../../aspose.words.bibliography/contributorcollection/translator/) { get; set; } | Gets or sets the translator of a source. |
| [Writer](../../aspose.words.bibliography/contributorcollection/writer/) { get; set; } | Gets or sets the writer of a source. |

## Examples

Shows how to get bibliography sources available in the document.

```csharp
Document document = new Document(MyDir + "Bibliography sources.docx");

Bibliography bibliography = document.Bibliography;
Assert.AreEqual(12, bibliography.Sources.Count);

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

* class [Contributor](../contributor/)
* namespace [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* assembly [Aspose.Words](../../)
