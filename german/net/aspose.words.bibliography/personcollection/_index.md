---
title: PersonCollection Class
linktitle: PersonCollection
articleTitle: PersonCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Bibliography.PersonCollection, die die Bibliografieverwaltung durch effiziente Auflistung der Quellenbeitragenden vereinfacht.
type: docs
weight: 190
url: /de/net/aspose.words.bibliography/personcollection/
---
## PersonCollection class

Stellt eine Liste von Personen dar, die zu den Quellen der Bibliografie beigetragen haben.

```csharp
public sealed class PersonCollection : Contributor, IEnumerable<Person>
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [PersonCollection](personcollection/#constructor)() | Initialisieren Sie eine neue Instanz des`PersonCollection` Klasse. |
| [PersonCollection](personcollection/#constructor_2)(*IEnumerable&lt;Person&gt;*) |  |
| [PersonCollection](personcollection/#constructor_1)(*params Person[]*) | Initialisieren Sie eine neue Instanz des`PersonCollection` Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.bibliography/personcollection/count/) { get; } | Ruft die Anzahl der in der Sammlung enthaltenen Personen ab. |
| [Item](../../aspose.words.bibliography/personcollection/item/) { get; set; } | Ruft eine Person am angegebenen Index ab oder legt sie fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.bibliography/personcollection/add/)(*[Person](../person/)*) | Fügt ein[`Person`](../person/) zur Sammlung. |
| [Clear](../../aspose.words.bibliography/personcollection/clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [Contains](../../aspose.words.bibliography/personcollection/contains/)(*[Person](../person/)*) | Bestimmt, ob die Sammlung eine bestimmte Person enthält. |
| [Remove](../../aspose.words.bibliography/personcollection/remove/)(*[Person](../person/)*) | Entfernt die Person aus der Sammlung. |
| [RemoveAt](../../aspose.words.bibliography/personcollection/removeat/)(*int*) | Entfernt die Person am angegebenen Index. |

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
* class [Person](../person/)
* namensraum [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* Montage [Aspose.Words](../../)
