---
title: ContributorCollection Class
linktitle: ContributorCollection
articleTitle: ContributorCollection
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Bibliography.ContributorCollection class to efficiently manage bibliography contributors and enhance your document's references.
type: docs
weight: 150
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
Assert.That(bibliography.Sources.Count, Is.EqualTo(12));

// Get default data from bibliography sources.
Source source = bibliography.Sources.FirstOrDefault();
Assert.That(source.Title, Is.EqualTo("Book 0 (No LCID)"));
Assert.That(source.SourceType, Is.EqualTo(SourceType.Book));
Assert.That(source.Contributors.Count(), Is.EqualTo(3));
Assert.That(source.AbbreviatedCaseNumber, Is.Null);
Assert.That(source.AlbumTitle, Is.Null);
Assert.That(source.BookTitle, Is.Null);
Assert.That(source.Broadcaster, Is.Null);
Assert.That(source.BroadcastTitle, Is.Null);
Assert.That(source.CaseNumber, Is.Null);
Assert.That(source.ChapterNumber, Is.Null);
Assert.That(source.Comments, Is.Null);
Assert.That(source.ConferenceName, Is.Null);
Assert.That(source.CountryOrRegion, Is.Null);
Assert.That(source.Court, Is.Null);
Assert.That(source.Day, Is.Null);
Assert.That(source.DayAccessed, Is.Null);
Assert.That(source.Department, Is.Null);
Assert.That(source.Distributor, Is.Null);
Assert.That(source.Doi, Is.Null);
Assert.That(source.Edition, Is.Null);
Assert.That(source.Guid, Is.Null);
Assert.That(source.Institution, Is.Null);
Assert.That(source.InternetSiteTitle, Is.Null);
Assert.That(source.Issue, Is.Null);
Assert.That(source.JournalName, Is.Null);
Assert.That(source.Lcid, Is.Null);
Assert.That(source.Medium, Is.Null);
Assert.That(source.Month, Is.Null);
Assert.That(source.MonthAccessed, Is.Null);
Assert.That(source.NumberVolumes, Is.Null);
Assert.That(source.Pages, Is.Null);
Assert.That(source.PatentNumber, Is.Null);
Assert.That(source.PeriodicalTitle, Is.Null);
Assert.That(source.ProductionCompany, Is.Null);
Assert.That(source.PublicationTitle, Is.Null);
Assert.That(source.Publisher, Is.Null);
Assert.That(source.RecordingNumber, Is.Null);
Assert.That(source.RefOrder, Is.Null);
Assert.That(source.Reporter, Is.Null);
Assert.That(source.ShortTitle, Is.Null);
Assert.That(source.StandardNumber, Is.Null);
Assert.That(source.StateOrProvince, Is.Null);
Assert.That(source.Station, Is.Null);
Assert.That(source.Tag, Is.EqualTo("BookNoLCID"));
Assert.That(source.Theater, Is.Null);
Assert.That(source.ThesisType, Is.Null);
Assert.That(source.Type, Is.Null);
Assert.That(source.Url, Is.Null);
Assert.That(source.Version, Is.Null);
Assert.That(source.Volume, Is.Null);
Assert.That(source.Year, Is.Null);
Assert.That(source.YearAccessed, Is.Null);

// Also, you can create a new source.
Source newSource = new Source("New source", SourceType.Misc);

ContributorCollection contributors = source.Contributors;
Assert.That(contributors.Artist, Is.Null);
Assert.That(contributors.BookAuthor, Is.Null);
Assert.That(contributors.Compiler, Is.Null);
Assert.That(contributors.Composer, Is.Null);
Assert.That(contributors.Conductor, Is.Null);
Assert.That(contributors.Counsel, Is.Null);
Assert.That(contributors.Director, Is.Null);
Assert.That(contributors.Editor, Is.Not.Null);
Assert.That(contributors.Interviewee, Is.Null);
Assert.That(contributors.Interviewer, Is.Null);
Assert.That(contributors.Inventor, Is.Null);
Assert.That(contributors.Performer, Is.Null);
Assert.That(contributors.Producer, Is.Null);
Assert.That(contributors.Translator, Is.Not.Null);
Assert.That(contributors.Writer, Is.Null);

Contributor editor  = contributors.Editor;
Assert.That(((PersonCollection)editor).Count(), Is.EqualTo(2));

PersonCollection authors = (PersonCollection)contributors.Author;
Assert.That(authors.Count(), Is.EqualTo(2));

Person person = authors[0];
Assert.That(person.First, Is.EqualTo("Roxanne"));
Assert.That(person.Middle, Is.EqualTo("Brielle"));
Assert.That(person.Last, Is.EqualTo("Tejeda"));
```

### See Also

* class [Contributor](../contributor/)
* namespace [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* assembly [Aspose.Words](../../)
