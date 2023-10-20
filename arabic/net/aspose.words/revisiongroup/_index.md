---
title: RevisionGroup Class
linktitle: RevisionGroup
articleTitle: RevisionGroup
second_title: Aspose.Words لـ .NET
description: Aspose.Words.RevisionGroup فصل. يمثل مجموعة متسلسلةRevision الكائنات في C#.
type: docs
weight: 4780
url: /ar/net/aspose.words/revisiongroup/
---
## RevisionGroup class

يمثل مجموعة متسلسلة[`Revision`](../revision/) الكائنات.

لمعرفة المزيد، قم بزيارة[تتبع التغييرات في مستند](https://docs.aspose.com/words/net/track-changes-in-a-document/) مقالة توثيقية.

```csharp
public class RevisionGroup
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Author](../../aspose.words/revisiongroup/author/) { get; } | الحصول على مؤلف مجموعة المراجعة هذه. |
| [RevisionType](../../aspose.words/revisiongroup/revisiontype/) { get; } | الحصول على نوع المراجعات المضمنة في هذه المجموعة. |
| [Text](../../aspose.words/revisiongroup/text/) { get; } | إرجاع النص المدرج/المحذوف/المنقول أو وصف تغيير التنسيق. |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
