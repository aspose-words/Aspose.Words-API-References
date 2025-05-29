---
title: PersonCollection Class
linktitle: PersonCollection
articleTitle: PersonCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Bibliography.PersonCollection، المصممة لتبسيط إدارة المراجع من خلال إدراج المساهمين في المصدر بكفاءة.
type: docs
weight: 190
url: /ar/net/aspose.words.bibliography/personcollection/
---
## PersonCollection class

يمثل قائمة الأشخاص الذين يساهمون في مصادر المراجع.

```csharp
public sealed class PersonCollection : Contributor, IEnumerable<Person>
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [PersonCollection](personcollection/#constructor)() | قم بتهيئة مثيل جديد لـ`PersonCollection` الصف. |
| [PersonCollection](personcollection/#constructor_2)(*IEnumerable&lt;Person&gt;*) |  |
| [PersonCollection](personcollection/#constructor_1)(*params Person[]*) | قم بتهيئة مثيل جديد لـ`PersonCollection` الصف. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.bibliography/personcollection/count/) { get; } | يحصل على عدد الأشخاص الموجودين في المجموعة. |
| [Item](../../aspose.words.bibliography/personcollection/item/) { get; set; } | يحصل على شخص أو يعينه عند الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.bibliography/personcollection/add/)(*[Person](../person/)*) | يضيف[`Person`](../person/) إلى المجموعة. |
| [Clear](../../aspose.words.bibliography/personcollection/clear/)() | يزيل جميع العناصر من المجموعة. |
| [Contains](../../aspose.words.bibliography/personcollection/contains/)(*[Person](../person/)*) | يحدد ما إذا كانت المجموعة تحتوي على شخص معين. |
| [Remove](../../aspose.words.bibliography/personcollection/remove/)(*[Person](../person/)*) | يزيل الشخص من المجموعة. |
| [RemoveAt](../../aspose.words.bibliography/personcollection/removeat/)(*int*) | يزيل الشخص الموجود في الفهرس المحدد. |

## أمثلة

يوضح كيفية الحصول على المصادر الببليوغرافية المتوفرة في المستند.

```csharp
Document document = new Document(MyDir + "Bibliography sources.docx");

Bibliography bibliography = document.Bibliography;
Assert.AreEqual(12, bibliography.Sources.Count);

// الحصول على البيانات الافتراضية من مصادر المراجع.
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

//يمكنك أيضًا إنشاء مصدر جديد.
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

### أنظر أيضا

* class [Contributor](../contributor/)
* class [Person](../person/)
* مساحة الاسم [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* المجسم [Aspose.Words](../../)
