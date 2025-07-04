---
title: Source.YearAccessed
linktitle: YearAccessed
articleTitle: YearAccessed
second_title: Aspose.Words for .NET
description: Manage your Source YearAccessed property easily. Get or set the accessed year for accurate citations and streamlined research management.
type: docs
weight: 540
url: /net/aspose.words.bibliography/source/yearaccessed/
---
## Source.YearAccessed property

Gets or sets the year accessed of a source.

```csharp
public string YearAccessed { get; set; }
```

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

* class [Source](../)
* namespace [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* assembly [Aspose.Words](../../../)
