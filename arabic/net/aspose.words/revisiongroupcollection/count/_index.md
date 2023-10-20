---
title: RevisionGroupCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words لـ .NET
description: RevisionGroupCollection Count ملكية. إرجاع عدد مجموعات المراجعة في المجموعة في C#.
type: docs
weight: 10
url: /ar/net/aspose.words/revisiongroupcollection/count/
---
## RevisionGroupCollection.Count property

إرجاع عدد مجموعات المراجعة في المجموعة.

```csharp
public int Count { get; }
```

## أمثلة

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

* class [RevisionGroupCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
