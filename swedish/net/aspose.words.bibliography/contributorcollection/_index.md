---
title: ContributorCollection Class
linktitle: ContributorCollection
articleTitle: ContributorCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Bibliography.ContributorCollection för att effektivt hantera bibliografiska bidragsgivare och förbättra dokumentets referenser.
type: docs
weight: 160
url: /sv/net/aspose.words.bibliography/contributorcollection/
---
## ContributorCollection class

Representerar bidragsgivare till bibliografikällor.

```csharp
public sealed class ContributorCollection : IEnumerable<Contributor>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Artist](../../aspose.words.bibliography/contributorcollection/artist/) { get; set; } | Hämtar eller ställer in artisten för en källa. |
| [Author](../../aspose.words.bibliography/contributorcollection/author/) { get; set; } | Hämtar eller anger författaren till en källa. |
| [BookAuthor](../../aspose.words.bibliography/contributorcollection/bookauthor/) { get; set; } | Hämtar eller anger bokens författare till en källa. |
| [Compiler](../../aspose.words.bibliography/contributorcollection/compiler/) { get; set; } | Hämtar eller ställer in kompilatorn för en källkod. |
| [Composer](../../aspose.words.bibliography/contributorcollection/composer/) { get; set; } | Hämtar eller ställer in kompositören för en källkod. |
| [Conductor](../../aspose.words.bibliography/contributorcollection/conductor/) { get; set; } | Hämtar eller ställer in ledaren för en källa. |
| [Counsel](../../aspose.words.bibliography/contributorcollection/counsel/) { get; set; } | Hämtar eller ställer in råd från en källa. |
| [Director](../../aspose.words.bibliography/contributorcollection/director/) { get; set; } | Hämtar eller ställer in direktören för en källa. |
| [Editor](../../aspose.words.bibliography/contributorcollection/editor/) { get; set; } | Hämtar eller ställer in redigeraren för en källa. |
| [Interviewee](../../aspose.words.bibliography/contributorcollection/interviewee/) { get; set; } | Hämtar eller ställer in en källas intervjuobjekt. |
| [Interviewer](../../aspose.words.bibliography/contributorcollection/interviewer/) { get; set; } | Hämtar eller ställer in intervjuaren för en källa. |
| [Inventor](../../aspose.words.bibliography/contributorcollection/inventor/) { get; set; } | Hämtar eller anger uppfinnaren av en källa. |
| [Performer](../../aspose.words.bibliography/contributorcollection/performer/) { get; set; } | Hämtar eller ställer in utföraren för en källa. |
| [Producer](../../aspose.words.bibliography/contributorcollection/producer/) { get; set; } | Hämtar eller anger producenten för en källa. |
| [Translator](../../aspose.words.bibliography/contributorcollection/translator/) { get; set; } | Hämtar eller ställer in översättaren för en källa. |
| [Writer](../../aspose.words.bibliography/contributorcollection/writer/) { get; set; } | Hämtar eller anger författaren till en källkod. |

## Exempel

Visar hur man får tillgång till litteraturkällor i dokumentet.

```csharp
Document document = new Document(MyDir + "Bibliography sources.docx");

Bibliography bibliography = document.Bibliography;
Assert.AreEqual(12, bibliography.Sources.Count);

// Hämta standarddata från bibliografiska källor.
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

// Du kan också skapa en ny källa.
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

### Se även

* class [Contributor](../contributor/)
* namnutrymme [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* hopsättning [Aspose.Words](../../)
