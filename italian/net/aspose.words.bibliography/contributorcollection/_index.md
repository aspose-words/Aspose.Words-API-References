---
title: ContributorCollection Class
linktitle: ContributorCollection
articleTitle: ContributorCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Bibliography.ContributorCollection per gestire in modo efficiente i collaboratori della bibliografia e migliorare i riferimenti del tuo documento.
type: docs
weight: 160
url: /it/net/aspose.words.bibliography/contributorcollection/
---
## ContributorCollection class

Rappresenta i contributori della fonte bibliografica.

```csharp
public sealed class ContributorCollection : IEnumerable<Contributor>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Artist](../../aspose.words.bibliography/contributorcollection/artist/) { get; set; } | Ottiene o imposta l'artista di una sorgente. |
| [Author](../../aspose.words.bibliography/contributorcollection/author/) { get; set; } | Ottiene o imposta l'autore di una fonte. |
| [BookAuthor](../../aspose.words.bibliography/contributorcollection/bookauthor/) { get; set; } | Ottiene o imposta l'autore del libro di una fonte. |
| [Compiler](../../aspose.words.bibliography/contributorcollection/compiler/) { get; set; } | Ottiene o imposta il compilatore di una sorgente. |
| [Composer](../../aspose.words.bibliography/contributorcollection/composer/) { get; set; } | Ottiene o imposta il compositore di una sorgente. |
| [Conductor](../../aspose.words.bibliography/contributorcollection/conductor/) { get; set; } | Ottiene o imposta il conduttore di una sorgente. |
| [Counsel](../../aspose.words.bibliography/contributorcollection/counsel/) { get; set; } | Ottiene o imposta il consiglio di una fonte. |
| [Director](../../aspose.words.bibliography/contributorcollection/director/) { get; set; } | Ottiene o imposta il direttore di una sorgente. |
| [Editor](../../aspose.words.bibliography/contributorcollection/editor/) { get; set; } | Ottiene o imposta l'editor di una sorgente. |
| [Interviewee](../../aspose.words.bibliography/contributorcollection/interviewee/) { get; set; } | Ottiene o imposta l'intervistato di una fonte. |
| [Interviewer](../../aspose.words.bibliography/contributorcollection/interviewer/) { get; set; } | Ottiene o imposta l'intervistatore di una fonte. |
| [Inventor](../../aspose.words.bibliography/contributorcollection/inventor/) { get; set; } | Ottiene o imposta l'inventore di una fonte. |
| [Performer](../../aspose.words.bibliography/contributorcollection/performer/) { get; set; } | Ottiene o imposta l'esecutore di una sorgente. |
| [Producer](../../aspose.words.bibliography/contributorcollection/producer/) { get; set; } | Ottiene o imposta il produttore di una sorgente. |
| [Translator](../../aspose.words.bibliography/contributorcollection/translator/) { get; set; } | Ottiene o imposta il traduttore di una sorgente. |
| [Writer](../../aspose.words.bibliography/contributorcollection/writer/) { get; set; } | Ottiene o imposta l'autore di una sorgente. |

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
* spazio dei nomi [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* assemblea [Aspose.Words](../../)
