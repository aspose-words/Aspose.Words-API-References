---
title: PersonCollection Class
linktitle: PersonCollection
articleTitle: PersonCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Bibliography.PersonCollection, progettata per semplificare la gestione delle bibliografie elencando in modo efficiente i contributori delle fonti.
type: docs
weight: 190
url: /it/net/aspose.words.bibliography/personcollection/
---
## PersonCollection class

Rappresenta un elenco di persone che hanno contribuito alla fonte bibliografica.

```csharp
public sealed class PersonCollection : Contributor, IEnumerable<Person>
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [PersonCollection](personcollection/#constructor)() | Inizializza una nuova istanza di`PersonCollection` classe. |
| [PersonCollection](personcollection/#constructor_2)(*IEnumerable&lt;Person&gt;*) |  |
| [PersonCollection](personcollection/#constructor_1)(*params Person[]*) | Inizializza una nuova istanza di`PersonCollection` classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.bibliography/personcollection/count/) { get; } | Ottiene il numero di persone contenute nella raccolta. |
| [Item](../../aspose.words.bibliography/personcollection/item/) { get; set; } | Ottiene o imposta una persona all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.bibliography/personcollection/add/)(*[Person](../person/)*) | Aggiunge un[`Person`](../person/) alla collezione. |
| [Clear](../../aspose.words.bibliography/personcollection/clear/)() | Rimuove tutti gli elementi dalla raccolta. |
| [Contains](../../aspose.words.bibliography/personcollection/contains/)(*[Person](../person/)*) | Determina se la raccolta contiene una persona specifica. |
| [Remove](../../aspose.words.bibliography/personcollection/remove/)(*[Person](../person/)*) | Rimuove la persona dalla raccolta. |
| [RemoveAt](../../aspose.words.bibliography/personcollection/removeat/)(*int*) | Rimuove la persona all'indice specificato. |

## Esempi

Mostra come ottenere le fonti bibliografiche disponibili nel documento.

```csharp
Document document = new Document(MyDir + "Bibliography sources.docx");

Bibliography bibliography = document.Bibliography;
Assert.AreEqual(12, bibliography.Sources.Count);

// Ottieni i dati predefiniti dalle fonti bibliografiche.
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

// Puoi anche creare una nuova sorgente.
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

### Guarda anche

* class [Contributor](../contributor/)
* class [Person](../person/)
* spazio dei nomi [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* assemblea [Aspose.Words](../../)
