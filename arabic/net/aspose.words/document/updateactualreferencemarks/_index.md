---
title: Document.UpdateActualReferenceMarks
linktitle: UpdateActualReferenceMarks
articleTitle: UpdateActualReferenceMarks
second_title: Aspose.Words لـ .NET
description: قم بتحديث جميع الحواشي السفلية والختامية في مستندك بسهولة باستخدام طريقة Document UpdateActualReferenceMarks، مما يعزز الدقة والكفاءة.
type: docs
weight: 800
url: /ar/net/aspose.words/document/updateactualreferencemarks/
---
## Document.UpdateActualReferenceMarks method

تحديث[`ActualReferenceMark`](../../../aspose.words.notes/footnote/actualreferencemark/) خاصية جميع الحواشي السفلية والختامية في المستند.

```csharp
public void UpdateActualReferenceMarks()
```

## ملاحظات

تحديث الحقول ([`UpdateFields`](../updatefields/) ) قد يكون ضروريًا للحصول على النتيجة الصحيحة.

## أمثلة

يوضح كيفية الحصول على علامة مرجعية فعلية للحاشية السفلية.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

Footnote footnote = (Footnote)doc.GetChild(NodeType.Footnote, 1, true);
doc.UpdateFields();
doc.UpdateActualReferenceMarks();

Assert.AreEqual("1", footnote.ActualReferenceMark);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
