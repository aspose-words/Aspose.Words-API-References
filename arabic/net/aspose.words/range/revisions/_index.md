---
title: Range.Revisions
linktitle: Revisions
articleTitle: Revisions
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة تعديلات النطاق. تتبع وأدر تغييرات العقارات بسهولة مع مجموعتنا الشاملة من التعديلات لتحسين وضوح المشروع.
type: docs
weight: 40
url: /ar/net/aspose.words/range/revisions/
---
## Range.Revisions property

يحصل على مجموعة من المراجعات (التغييرات المتعقبة) الموجودة في هذا النطاق.

```csharp
public RevisionCollection Revisions { get; }
```

## ملاحظات

المجموعة المرتجعة هي مجموعة "حية"، مما يعني أنه إذا قمت بإزالة أجزاء من مستند تحتوي على إصدارات، فستختفي الإصدارات المحذوفة تلقائيًا من هذه المجموعة.

## أمثلة

يوضح كيفية العمل مع المراجعات في النطاق.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
foreach (Revision revision in paragraph.Range.Revisions)
{
    if (revision.RevisionType == RevisionType.Deletion)
        revision.Accept();
}

// رفض المراجعات الخاصة بالقسم الأول.
doc.FirstSection.Range.Revisions.RejectAll();
```

### أنظر أيضا

* class [RevisionCollection](../../revisioncollection/)
* class [Range](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
