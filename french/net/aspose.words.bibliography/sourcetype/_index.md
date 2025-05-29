---
title: SourceType Enum
linktitle: SourceType
articleTitle: SourceType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Bibliography.SourceType pour divers types de sources bibliographiques. Améliorez la gestion de vos documents grâce à de puissantes fonctionnalités !
type: docs
weight: 210
url: /fr/net/aspose.words.bibliography/sourcetype/
---
## SourceType enumeration

Représente les types de sources bibliographiques.

```csharp
public enum SourceType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| ArticleInAPeriodical | `0` | Spécifie l'article dans une source périodique. |
| Book | `1` | Spécifie la source du livre. |
| BookSection | `2` | Spécifie la source de la section du livre. |
| JournalArticle | `3` | Spécifie la source de l'article de journal. |
| ConferenceProceedings | `4` | Spécifie la source des actes de la conférence. |
| Report | `5` | Spécifie la source du rapporteur. |
| SoundRecording | `6` | Spécifie la source d'enregistrement sonore. |
| Performance | `7` | Spécifie la source de performance. |
| Art | `8` | Spécifie la source de l'illustration. |
| DocumentFromInternetSite | `9` | Spécifie le document provenant de la source du site Internet. |
| InternetSite | `10` | Spécifie la source du site Internet. |
| Film | `11` | Spécifie la source du film. |
| Interview | `12` | Spécifie la source de l'interview. |
| Patent | `13` | Spécifie la source du brevet. |
| Electronic | `14` | Spécifie la source électronique. |
| Case | `15` | Spécifie la source du cas. |
| Misc | `16` | Spécifie la source diverse. |

## Exemples

Montre comment obtenir les sources bibliographiques disponibles dans le document.

```csharp
Document document = new Document(MyDir + "Bibliography sources.docx");

Bibliography bibliography = document.Bibliography;
Assert.AreEqual(12, bibliography.Sources.Count);

// Obtenir les données par défaut à partir des sources bibliographiques.
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

// Vous pouvez également créer une nouvelle source.
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

### Voir également

* espace de noms [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* Assemblée [Aspose.Words](../../)
