---
title: SourceType Enum
linktitle: SourceType
articleTitle: SourceType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Bibliography.SourceType 枚举，支持多种参考文献源类型。使用强大的功能增强您的文档管理！
type: docs
weight: 210
url: /zh/net/aspose.words.bibliography/sourcetype/
---
## SourceType enumeration

代表参考书目来源类型。

```csharp
public enum SourceType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| ArticleInAPeriodical | `0` | 指定期刊来源中的文章。 |
| Book | `1` | 指定书籍来源。 |
| BookSection | `2` | 指定书籍章节来源。 |
| JournalArticle | `3` | 指定期刊文章来源。 |
| ConferenceProceedings | `4` | 指定会议记录来源。 |
| Report | `5` | 指定报告源。 |
| SoundRecording | `6` | 指定录音源。 |
| Performance | `7` | 指定性能源。 |
| Art | `8` | 指定艺术来源。 |
| DocumentFromInternetSite | `9` | 指定来自互联网站点源的文档。 |
| InternetSite | `10` | 指定互联网站点源。 |
| Film | `11` | 指定影片来源。 |
| Interview | `12` | 指定采访来源。 |
| Patent | `13` | 指定专利来源。 |
| Electronic | `14` | 指定电子源。 |
| Case | `15` | 指定案例来源。 |
| Misc | `16` | 指定杂项来源。 |

## 例子

展示如何获取文档中可用的参考书目来源。

```csharp
Document document = new Document(MyDir + "Bibliography sources.docx");

Bibliography bibliography = document.Bibliography;
Assert.AreEqual(12, bibliography.Sources.Count);

// 从参考书目来源获取默认数据。
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

// 另外，您还可以创建一个新的源。
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

### 也可以看看

* 命名空间 [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* 部件 [Aspose.Words](../../)
