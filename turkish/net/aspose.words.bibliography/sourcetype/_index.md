---
title: SourceType Enum
linktitle: SourceType
articleTitle: SourceType
second_title: .NET için Aspose.Words
description: Çeşitli bibliyografya kaynak türleri için Aspose.Words.Bibliography.SourceType enum'unu keşfedin. Güçlü özelliklerle belge yönetiminizi geliştirin!
type: docs
weight: 210
url: /tr/net/aspose.words.bibliography/sourcetype/
---
## SourceType enumeration

Bibliyografya kaynak türlerini temsil eder.

```csharp
public enum SourceType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| ArticleInAPeriodical | `0` | Makaleyi süreli bir kaynakta belirtir. |
| Book | `1` | Kitap kaynağını belirtir. |
| BookSection | `2` | Kitap bölümü kaynağını belirtir. |
| JournalArticle | `3` | Dergi makalesi kaynağını belirtir. |
| ConferenceProceedings | `4` | Konferans bildirilerinin kaynağını belirtir. |
| Report | `5` | Muhabir kaynağını belirtir. |
| SoundRecording | `6` | Ses kayıt kaynağını belirtir. |
| Performance | `7` | Performans kaynağını belirtir. |
| Art | `8` | Sanat kaynağını belirtir. |
| DocumentFromInternetSite | `9` | İnternet sitesi kaynağından gelen belgeyi belirtir. |
| InternetSite | `10` | İnternet sitesi kaynağını belirtir. |
| Film | `11` | Film kaynağını belirtir. |
| Interview | `12` | Röportaj kaynağını belirtir. |
| Patent | `13` | Patent kaynağını belirtir. |
| Electronic | `14` | Elektronik kaynağı belirtir. |
| Case | `15` | Durum kaynağını belirtir. |
| Misc | `16` | Çeşitli kaynağı belirtir. |

## Örnekler

Belgede bulunan bibliyografya kaynaklarının nasıl alınacağını gösterir.

```csharp
Document document = new Document(MyDir + "Bibliography sources.docx");

Bibliography bibliography = document.Bibliography;
Assert.AreEqual(12, bibliography.Sources.Count);

// Bibliyografya kaynaklarından varsayılan verileri al.
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

// Ayrıca yeni bir kaynak da oluşturabilirsiniz.
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

### Ayrıca bakınız

* ad alanı [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* toplantı [Aspose.Words](../../)
