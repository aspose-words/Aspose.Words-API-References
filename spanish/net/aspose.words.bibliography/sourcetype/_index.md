---
title: SourceType Enum
linktitle: SourceType
articleTitle: SourceType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Bibliography.SourceType para diversos tipos de fuentes bibliográficas. ¡Mejore su gestión documental con potentes funciones!
type: docs
weight: 210
url: /es/net/aspose.words.bibliography/sourcetype/
---
## SourceType enumeration

Representa los tipos de fuentes bibliográficas.

```csharp
public enum SourceType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| ArticleInAPeriodical | `0` | Especifica el artículo en una fuente periódica. |
| Book | `1` | Especifica la fuente del libro. |
| BookSection | `2` | Especifica la fuente de la sección del libro. |
| JournalArticle | `3` | Especifica la fuente del artículo de la revista. |
| ConferenceProceedings | `4` | Especifica la fuente de las actas de la conferencia. |
| Report | `5` | Especifica la fuente del reportero. |
| SoundRecording | `6` | Especifica la fuente de grabación de sonido. |
| Performance | `7` | Especifica la fuente de rendimiento. |
| Art | `8` | Especifica la fuente del arte. |
| DocumentFromInternetSite | `9` | Especifica el documento de origen del sitio de Internet. |
| InternetSite | `10` | Especifica la fuente del sitio de Internet. |
| Film | `11` | Especifica la fuente de la película. |
| Interview | `12` | Especifica la fuente de la entrevista. |
| Patent | `13` | Especifica la fuente de la patente. |
| Electronic | `14` | Especifica la fuente electrónica. |
| Case | `15` | Especifica la fuente del caso. |
| Misc | `16` | Especifica la fuente miscelánea. |

## Ejemplos

Muestra cómo obtener fuentes bibliográficas disponibles en el documento.

```csharp
Document document = new Document(MyDir + "Bibliography sources.docx");

Bibliography bibliography = document.Bibliography;
Assert.AreEqual(12, bibliography.Sources.Count);

// Obtener datos predeterminados de fuentes bibliográficas.
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

//También puedes crear una nueva fuente.
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

### Ver también

* espacio de nombres [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* asamblea [Aspose.Words](../../)
