---
title: RevisionGroup.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words لـ .NET
description: RevisionGroup Author ملكية. الحصول على مؤلف مجموعة المراجعة هذه في C#.
type: docs
weight: 10
url: /ar/net/aspose.words/revisiongroup/author/
---
## RevisionGroup.Author property

الحصول على مؤلف مجموعة المراجعة هذه.

```csharp
public string Author { get; }
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

* class [RevisionGroup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
