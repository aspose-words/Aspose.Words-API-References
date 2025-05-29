---
title: ContributorCollection Class
linktitle: ContributorCollection
articleTitle: ContributorCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Bibliography.ContributorCollection, um Bibliografie-Mitwirkende effizient zu verwalten und die Referenzen Ihres Dokuments zu verbessern.
type: docs
weight: 160
url: /de/net/aspose.words.bibliography/contributorcollection/
---
## ContributorCollection class

Stellt die Mitwirkenden der Bibliografiequelle dar.

```csharp
public sealed class ContributorCollection : IEnumerable<Contributor>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Artist](../../aspose.words.bibliography/contributorcollection/artist/) { get; set; } | Ruft den Interpreten einer Quelle ab oder legt ihn fest. |
| [Author](../../aspose.words.bibliography/contributorcollection/author/) { get; set; } | Ruft den Autor einer Quelle ab oder legt ihn fest. |
| [BookAuthor](../../aspose.words.bibliography/contributorcollection/bookauthor/) { get; set; } | Ruft den Buchautor einer Quelle ab oder legt ihn fest. |
| [Compiler](../../aspose.words.bibliography/contributorcollection/compiler/) { get; set; } | Ruft den Compiler einer Quelle ab oder legt ihn fest. |
| [Composer](../../aspose.words.bibliography/contributorcollection/composer/) { get; set; } | Ruft den Komponisten einer Quelle ab oder legt ihn fest. |
| [Conductor](../../aspose.words.bibliography/contributorcollection/conductor/) { get; set; } | Ruft den Leiter einer Quelle ab oder legt ihn fest. |
| [Counsel](../../aspose.words.bibliography/contributorcollection/counsel/) { get; set; } | Ruft den Rat einer Quelle ab oder legt ihn fest. |
| [Director](../../aspose.words.bibliography/contributorcollection/director/) { get; set; } | Ruft den Direktor einer Quelle ab oder legt ihn fest. |
| [Editor](../../aspose.words.bibliography/contributorcollection/editor/) { get; set; } | Ruft den Editor einer Quelle ab oder legt ihn fest. |
| [Interviewee](../../aspose.words.bibliography/contributorcollection/interviewee/) { get; set; } | Ruft den Interviewpartner einer Quelle ab oder legt ihn fest. |
| [Interviewer](../../aspose.words.bibliography/contributorcollection/interviewer/) { get; set; } | Ruft den Interviewer einer Quelle ab oder legt ihn fest. |
| [Inventor](../../aspose.words.bibliography/contributorcollection/inventor/) { get; set; } | Ruft den Erfinder einer Quelle ab oder legt ihn fest. |
| [Performer](../../aspose.words.bibliography/contributorcollection/performer/) { get; set; } | Ruft den Ausführenden einer Quelle ab oder legt ihn fest. |
| [Producer](../../aspose.words.bibliography/contributorcollection/producer/) { get; set; } | Ruft den Produzenten einer Quelle ab oder legt ihn fest. |
| [Translator](../../aspose.words.bibliography/contributorcollection/translator/) { get; set; } | Ruft den Übersetzer einer Quelle ab oder legt ihn fest. |
| [Writer](../../aspose.words.bibliography/contributorcollection/writer/) { get; set; } | Ruft den Writer einer Quelle ab oder legt ihn fest. |

## Beispiele

Zeigt, wie man im Dokument verfügbare Bibliografiequellen erhält.

```csharp
Document document = new Document(MyDir + "Bibliography sources.docx");

Bibliography bibliography = document.Bibliography;
Assert.AreEqual(12, bibliography.Sources.Count);

// Standarddaten aus Bibliografiequellen abrufen.
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

// Sie können auch eine neue Quelle erstellen.
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

### Siehe auch

* class [Contributor](../contributor/)
* namensraum [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* Montage [Aspose.Words](../../)
