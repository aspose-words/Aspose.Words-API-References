---
title: ContributorCollection Class
linktitle: ContributorCollection
articleTitle: ContributorCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Bibliography.ContributorCollection 类，以有效管理参考书目贡献者并增强文档的参考。
type: docs
weight: 160
url: /zh/net/aspose.words.bibliography/contributorcollection/
---
## ContributorCollection class

代表参考书目来源贡献者。

```csharp
public sealed class ContributorCollection : IEnumerable<Contributor>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Artist](../../aspose.words.bibliography/contributorcollection/artist/) { get; set; } | 获取或设置来源的艺术家。 |
| [Author](../../aspose.words.bibliography/contributorcollection/author/) { get; set; } | 获取或设置来源的作者。 |
| [BookAuthor](../../aspose.words.bibliography/contributorcollection/bookauthor/) { get; set; } | 获取或设置来源的书籍作者。 |
| [Compiler](../../aspose.words.bibliography/contributorcollection/compiler/) { get; set; } | 获取或设置源的编译器。 |
| [Composer](../../aspose.words.bibliography/contributorcollection/composer/) { get; set; } | 获取或设置源的作曲家。 |
| [Conductor](../../aspose.words.bibliography/contributorcollection/conductor/) { get; set; } | 获取或设置源的导体。 |
| [Counsel](../../aspose.words.bibliography/contributorcollection/counsel/) { get; set; } | 获取或设置来源的建议。 |
| [Director](../../aspose.words.bibliography/contributorcollection/director/) { get; set; } | 获取或设置源的导演。 |
| [Editor](../../aspose.words.bibliography/contributorcollection/editor/) { get; set; } | 获取或设置源的编辑器。 |
| [Interviewee](../../aspose.words.bibliography/contributorcollection/interviewee/) { get; set; } | 获取或设置来源的受访者。 |
| [Interviewer](../../aspose.words.bibliography/contributorcollection/interviewer/) { get; set; } | 获取或设置来源的采访者。 |
| [Inventor](../../aspose.words.bibliography/contributorcollection/inventor/) { get; set; } | 获取或设置来源的发明者。 |
| [Performer](../../aspose.words.bibliography/contributorcollection/performer/) { get; set; } | 获取或设置源的执行者。 |
| [Producer](../../aspose.words.bibliography/contributorcollection/producer/) { get; set; } | 获取或设置源的生产者。 |
| [Translator](../../aspose.words.bibliography/contributorcollection/translator/) { get; set; } | 获取或设置源的转换器。 |
| [Writer](../../aspose.words.bibliography/contributorcollection/writer/) { get; set; } | 获取或设置源的编写者。 |

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

* class [Contributor](../contributor/)
* 命名空间 [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* 部件 [Aspose.Words](../../)
