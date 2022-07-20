---
title: Text
second_title: Aspose.Words لمراجع .NET API
description: إرجاع النص الذي تم إدخاله / حذفه / نقله أو وصف تغيير التنسيق.
type: docs
weight: 30
url: /ar/net/aspose.words/revisiongroup/text/
---
## RevisionGroup.Text property

إرجاع النص الذي تم إدخاله / حذفه / نقله أو وصف تغيير التنسيق.

```csharp
public string Text { get; }
```

### أمثلة

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

* class [RevisionGroup](../../revisiongroup)
* مساحة الاسم [Aspose.Words](../../revisiongroup)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->