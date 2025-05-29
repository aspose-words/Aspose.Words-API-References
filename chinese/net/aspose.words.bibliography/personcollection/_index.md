---
title: PersonCollection Class
linktitle: PersonCollection
articleTitle: PersonCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Bibliography.PersonCollection 类，旨在通过有效列出源贡献者来简化参考书目管理。
type: docs
weight: 190
url: /zh/net/aspose.words.bibliography/personcollection/
---
## PersonCollection class

代表参考书目来源贡献者的名单。

```csharp
public sealed class PersonCollection : Contributor, IEnumerable<Person>
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [PersonCollection](personcollection/#constructor)() | 初始化`PersonCollection`类. |
| [PersonCollection](personcollection/#constructor_2)(*IEnumerable&lt;Person&gt;*) |  |
| [PersonCollection](personcollection/#constructor_1)(*params Person[]*) | 初始化`PersonCollection`类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.bibliography/personcollection/count/) { get; } | 获取集合中包含的人数。 |
| [Item](../../aspose.words.bibliography/personcollection/item/) { get; set; } | 获取或设置指定索引处的人。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.bibliography/personcollection/add/)(*[Person](../person/)*) | 添加[`Person`](../person/)到收藏夹。 |
| [Clear](../../aspose.words.bibliography/personcollection/clear/)() | 从集合中删除所有项目。 |
| [Contains](../../aspose.words.bibliography/personcollection/contains/)(*[Person](../person/)*) | 确定集合是否包含特定的人。 |
| [Remove](../../aspose.words.bibliography/personcollection/remove/)(*[Person](../person/)*) | 从集合中移除该人。 |
| [RemoveAt](../../aspose.words.bibliography/personcollection/removeat/)(*int*) | 删除指定索引处的人。 |

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
* class [Person](../person/)
* 命名空间 [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* 部件 [Aspose.Words](../../)
