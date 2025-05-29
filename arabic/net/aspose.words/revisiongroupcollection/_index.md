---
title: RevisionGroupCollection Class
linktitle: RevisionGroupCollection
articleTitle: RevisionGroupCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.RevisionGroupCollection، التي تتميز بإدارة فعالة لمجموعات مراجعة المستندات لتحسين التحرير والتعاون.
type: docs
weight: 5530
url: /ar/net/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class

مجموعة من[`RevisionGroup`](../revisiongroup/)الكائنات التي تمثل مجموعات المراجعة في المستند.

لمعرفة المزيد، قم بزيارة[تعقب التغييرات في المستند](https://docs.aspose.com/words/net/track-changes-in-a-document/) مقالة توثيقية.

```csharp
public sealed class RevisionGroupCollection : IEnumerable<RevisionGroup>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/revisiongroupcollection/count/) { get; } | يعيد عدد مجموعات المراجعة في المجموعة. |
| [Item](../../aspose.words/revisiongroupcollection/item/) { get; } | يعيد مجموعة المراجعة عند الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetEnumerator](../../aspose.words/revisiongroupcollection/getenumerator/)() | يعيد كائن المعداد. |

## ملاحظات

لا يمكنك إنشاء مثيلات لهذه الفئة مباشرةً. استخدم[`Groups`](../revisioncollection/groups/) الخاصية للحصول على مجموعات المراجعة الموجودة في المستند.

## أمثلة

يوضح كيفية الحصول على مجموعة من المراجعات في مستند.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

يوضح كيفية طباعة المعلومات حول مجموعة من المراجعات في مستند.

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
