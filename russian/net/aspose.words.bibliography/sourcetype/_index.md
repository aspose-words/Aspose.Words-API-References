---
title: SourceType Enum
linktitle: SourceType
articleTitle: SourceType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Bibliography.SourceType для различных типов источников библиографии. Улучшите управление документами с помощью мощных функций!
type: docs
weight: 210
url: /ru/net/aspose.words.bibliography/sourcetype/
---
## SourceType enumeration

Представляет типы источников библиографии.

```csharp
public enum SourceType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| ArticleInAPeriodical | `0` | Указывает статью в периодическом издании. |
| Book | `1` | Указывает источник книги. |
| BookSection | `2` | Указывает источник раздела книги. |
| JournalArticle | `3` | Указывает источник журнальной статьи. |
| ConferenceProceedings | `4` | Указывает источник материалов конференции. |
| Report | `5` | Указывает источник репортера. |
| SoundRecording | `6` | Указывает источник записи звука. |
| Performance | `7` | Указывает источник производительности. |
| Art | `8` | Указывает источник искусства. |
| DocumentFromInternetSite | `9` | Указывает документ из источника интернет-сайта. |
| InternetSite | `10` | Указывает источник интернет-сайта. |
| Film | `11` | Указывает источник фильма. |
| Interview | `12` | Указывает источник интервью. |
| Patent | `13` | Указывает источник патента. |
| Electronic | `14` | Указывает электронный источник. |
| Case | `15` | Указывает источник дела. |
| Misc | `16` | Указывает другой источник. |

## Примеры

Показывает, как получить доступ к библиографическим источникам в документе.

```csharp
Document document = new Document(MyDir + "Bibliography sources.docx");

Bibliography bibliography = document.Bibliography;
Assert.AreEqual(12, bibliography.Sources.Count);

// Получить данные по умолчанию из источников библиографии.
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

// Также вы можете создать новый источник.
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

### Смотрите также

* пространство имен [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* сборка [Aspose.Words](../../)
