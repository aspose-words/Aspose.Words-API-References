---
title: Range.Revisions
second_title: Aspose.Words لمراجع .NET API
description: Range ملكية. الحصول على مجموعة من المراجعات التغييرات المتعقبة الموجودة في هذا النطاق.
type: docs
weight: 40
url: /ar/net/aspose.words/range/revisions/
---
## Range.Revisions property

الحصول على مجموعة من المراجعات (التغييرات المتعقبة) الموجودة في هذا النطاق.

```csharp
public RevisionCollection Revisions { get; }
```

### ملاحظات

المجموعة التي تم إرجاعها هي مجموعة "مباشرة"، مما يعني أنه إذا قمت بإزالة أجزاء من مستند يحتوي على مراجعات ، فإن المراجعات المحذوفة ستختفي تلقائيًا من هذه المجموعة.

### أمثلة

يوضح كيفية العمل مع المراجعات في النطاق.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
foreach (Revision revision in paragraph.Range.Revisions)
{
    if (revision.RevisionType == RevisionType.Deletion)
        revision.Accept();
}

// رفض مراجعات القسم الأول.
doc.FirstSection.Range.Revisions.RejectAll();
```

### أنظر أيضا

* class [RevisionCollection](../../revisioncollection/)
* class [Range](../)
* مساحة الاسم [Aspose.Words](../../range/)
* المجسم [Aspose.Words](../../../)


