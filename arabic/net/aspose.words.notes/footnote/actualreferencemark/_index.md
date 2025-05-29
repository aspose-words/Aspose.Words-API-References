---
title: Footnote.ActualReferenceMark
linktitle: ActualReferenceMark
articleTitle: ActualReferenceMark
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Footnote ActualReferenceMark للوصول إلى النص الدقيق لعلامات المرجع في مستنداتك، مما يعزز الوضوح والتنظيم.
type: docs
weight: 20
url: /ar/net/aspose.words.notes/footnote/actualreferencemark/
---
## Footnote.ActualReferenceMark property

يحصل على النص الفعلي لعلامة المرجع المعروضة في المستند لهذه الحاشية السفلية.

```csharp
public string ActualReferenceMark { get; }
```

## ملاحظات

لتعبئة قيم هذه الخاصية مبدئيًا لجميع علامات المرجع في المستند، أو لتحديث القيم بعد التغييرات في المستند التي قد تؤثر على علامات المرجع، يجب عليك تنفيذ [`UpdateActualReferenceMarks`](../../../aspose.words/document/updateactualreferencemarks/) الطريقة. تحديث الحقول ([`UpdateFields`](../../../aspose.words/document/updatefields/) ) قد يكون ضروريًا أيضًا للحصول على النتيجة الصحيحة.

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

* class [Footnote](../)
* مساحة الاسم [Aspose.Words.Notes](../../../aspose.words.notes/)
* المجسم [Aspose.Words](../../../)
