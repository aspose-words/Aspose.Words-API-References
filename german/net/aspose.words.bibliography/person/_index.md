---
title: Person Class
linktitle: Person
articleTitle: Person
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Bibliography.Person zur Verwaltung einzelner Mitwirkender in Bibliografien. Verbessern Sie die Zitatgenauigkeit Ihres Dokuments!
type: docs
weight: 180
url: /de/net/aspose.words.bibliography/person/
---
## Person class

Stellt einen einzelnen (eine Person) Beitragenden zur Bibliografiequelle dar.

```csharp
public sealed class Person
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Person](person/)(*string, string, string*) | Initialisieren Sie eine neue Instanz des`Person` Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [First](../../aspose.words.bibliography/person/first/) { get; set; } | Ruft den Vornamen einer Person ab oder legt ihn fest. |
| [Last](../../aspose.words.bibliography/person/last/) { get; set; } | Ruft den Nachnamen einer Person ab oder legt ihn fest. |
| [Middle](../../aspose.words.bibliography/person/middle/) { get; set; } | Ruft den zweiten Vornamen einer Person ab oder legt ihn fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Equals](../../aspose.words.bibliography/person/equals/)(*object*) |  |
| override [GetHashCode](../../aspose.words.bibliography/person/gethashcode/)() |  |

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

* namensraum [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* Montage [Aspose.Words](../../)
