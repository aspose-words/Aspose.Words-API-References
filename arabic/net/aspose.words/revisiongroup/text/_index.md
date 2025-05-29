---
title: RevisionGroup.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: استكشف خاصية النص RevisionGroup للوصول إلى النص المدرج أو المحذوف أو المنقول، مما يعزز رؤى تنسيق المستند وكفاءة التحرير.
type: docs
weight: 30
url: /ar/net/aspose.words/revisiongroup/text/
---
## RevisionGroup.Text property

إرجاع النص المدرج/المحذوف/المنقول أو وصف تغيير التنسيق.

```csharp
public string Text { get; }
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

* class [RevisionGroup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
