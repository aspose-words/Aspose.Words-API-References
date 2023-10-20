---
title: RevisionGroupCollection Class
linktitle: RevisionGroupCollection
articleTitle: RevisionGroupCollection
second_title: Aspose.Words لـ .NET
description: Aspose.Words.RevisionGroupCollection فصل. مجموعة منRevisionGroup الكائنات التي تمثل مجموعات المراجعة في المستند في C#.
type: docs
weight: 4790
url: /ar/net/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class

مجموعة من[`RevisionGroup`](../revisiongroup/) الكائنات التي تمثل مجموعات المراجعة في المستند.

لمعرفة المزيد، قم بزيارة[تتبع التغييرات في مستند](https://docs.aspose.com/words/net/track-changes-in-a-document/) مقالة توثيقية.

```csharp
public sealed class RevisionGroupCollection : IEnumerable<RevisionGroup>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/revisiongroupcollection/count/) { get; } | إرجاع عدد مجموعات المراجعة في المجموعة. |
| [Item](../../aspose.words/revisiongroupcollection/item/) { get; } | إرجاع مجموعة المراجعة في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetEnumerator](../../aspose.words/revisiongroupcollection/getenumerator/)() | يُرجع كائن العداد. |

## ملاحظات

لا تقم بإنشاء مثيلات هذه الفئة مباشرة. استخدم ال[`Groups`](../revisioncollection/groups/) خاصية للحصول على مجموعات المراجعة الموجودة في المستند.

## أمثلة

يوضح كيفية الحصول على مجموعة من المراجعات في مستند.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

يوضح كيفية طباعة معلومات حول مجموعة من المراجعات في مستند.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Assert.AreEqual(7, doc.Revisions.Groups.Count);

foreach (RevisionGroup group in doc.Revisions.Groups)
{
    Console.WriteLine(
        $"Revision author: {group.Author}; Revision type: {group.RevisionType} \n\tRevision text: {group.Text}");
}
```

### أنظر أيضا

* class [RevisionGroup](../revisiongroup/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
