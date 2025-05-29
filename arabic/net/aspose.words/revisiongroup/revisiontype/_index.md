---
title: RevisionGroup.RevisionType
linktitle: RevisionType
articleTitle: RevisionType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية RevisionGroup RevisionType لتحديد أنواع المراجعات في مشروعك وإدارتها بسهولة. بسّط سير عملك اليوم!
type: docs
weight: 20
url: /ar/net/aspose.words/revisiongroup/revisiontype/
---
## RevisionGroup.RevisionType property

يحصل على نوع المراجعات المضمنة في هذه المجموعة.

```csharp
public RevisionType RevisionType { get; }
```

## أمثلة

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

* enum [RevisionType](../../revisiontype/)
* class [RevisionGroup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
