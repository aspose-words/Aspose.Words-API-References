---
title: ContributorCollection Class
linktitle: ContributorCollection
articleTitle: ContributorCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Bibliography.ContributorCollection para administrar de manera eficiente los contribuyentes a la bibliografía y mejorar las referencias de sus documentos.
type: docs
weight: 160
url: /es/net/aspose.words.bibliography/contributorcollection/
---
## ContributorCollection class

Representa a los contribuyentes de las fuentes bibliográficas.

```csharp
public sealed class ContributorCollection : IEnumerable<Contributor>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Artist](../../aspose.words.bibliography/contributorcollection/artist/) { get; set; } | Obtiene o establece el artista de una fuente. |
| [Author](../../aspose.words.bibliography/contributorcollection/author/) { get; set; } | Obtiene o establece el autor de una fuente. |
| [BookAuthor](../../aspose.words.bibliography/contributorcollection/bookauthor/) { get; set; } | Obtiene o establece el autor del libro de una fuente. |
| [Compiler](../../aspose.words.bibliography/contributorcollection/compiler/) { get; set; } | Obtiene o establece el compilador de una fuente. |
| [Composer](../../aspose.words.bibliography/contributorcollection/composer/) { get; set; } | Obtiene o establece el compositor de una fuente. |
| [Conductor](../../aspose.words.bibliography/contributorcollection/conductor/) { get; set; } | Obtiene o establece el conductor de una fuente. |
| [Counsel](../../aspose.words.bibliography/contributorcollection/counsel/) { get; set; } | Obtiene o establece el consejo de una fuente. |
| [Director](../../aspose.words.bibliography/contributorcollection/director/) { get; set; } | Obtiene o establece el director de una fuente. |
| [Editor](../../aspose.words.bibliography/contributorcollection/editor/) { get; set; } | Obtiene o establece el editor de una fuente. |
| [Interviewee](../../aspose.words.bibliography/contributorcollection/interviewee/) { get; set; } | Obtiene o establece el entrevistado de una fuente. |
| [Interviewer](../../aspose.words.bibliography/contributorcollection/interviewer/) { get; set; } | Obtiene o establece el entrevistador de una fuente. |
| [Inventor](../../aspose.words.bibliography/contributorcollection/inventor/) { get; set; } | Obtiene o establece el inventor de una fuente. |
| [Performer](../../aspose.words.bibliography/contributorcollection/performer/) { get; set; } | Obtiene o establece el ejecutante de una fuente. |
| [Producer](../../aspose.words.bibliography/contributorcollection/producer/) { get; set; } | Obtiene o establece el productor de una fuente. |
| [Translator](../../aspose.words.bibliography/contributorcollection/translator/) { get; set; } | Obtiene o establece el traductor de una fuente. |
| [Writer](../../aspose.words.bibliography/contributorcollection/writer/) { get; set; } | Obtiene o establece el escritor de una fuente. |

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

* class [Contributor](../contributor/)
* espacio de nombres [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* asamblea [Aspose.Words](../../)
