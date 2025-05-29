---
title: SourceType Enum
linktitle: SourceType
articleTitle: SourceType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Bibliography.SourceType per diversi tipi di fonti bibliografiche. Migliora la gestione dei tuoi documenti con potenti funzionalità!
type: docs
weight: 210
url: /it/net/aspose.words.bibliography/sourcetype/
---
## SourceType enumeration

Rappresenta i tipi di fonte bibliografica.

```csharp
public enum SourceType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| ArticleInAPeriodical | `0` | Specifica l'articolo in una fonte periodica. |
| Book | `1` | Specifica la fonte del libro. |
| BookSection | `2` | Specifica la fonte della sezione del libro. |
| JournalArticle | `3` | Specifica la fonte dell'articolo di giornale. |
| ConferenceProceedings | `4` | Specifica la fonte degli atti della conferenza. |
| Report | `5` | Specifica la fonte del reporter. |
| SoundRecording | `6` | Specifica la sorgente di registrazione audio. |
| Performance | `7` | Specifica la sorgente delle prestazioni. |
| Art | `8` | Specifica la fonte artistica. |
| DocumentFromInternetSite | `9` | Specifica il documento dalla fonte del sito Internet. |
| InternetSite | `10` | Specifica la fonte del sito Internet. |
| Film | `11` | Specifica la sorgente del film. |
| Interview | `12` | Specifica la fonte dell'intervista. |
| Patent | `13` | Specifica la fonte del brevetto. |
| Electronic | `14` | Specifica la sorgente elettronica. |
| Case | `15` | Specifica l'origine del caso. |
| Misc | `16` | Specifica la fonte varia. |

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

* spazio dei nomi [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* assemblea [Aspose.Words](../../)
