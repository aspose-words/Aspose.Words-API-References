---
title: RevisionsView Enum
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.RevisionsView enum لاختيار بسهولة بين إصدارات المستند الأصلية والمنقحة لتسهيل التحرير والتعاون.
type: docs
weight: 5550
url: /ar/net/aspose.words/revisionsview/
---
## RevisionsView enumeration

يسمح بتحديد ما إذا كان سيتم العمل مع الإصدار الأصلي أو المنقح للمستند.

```csharp
public enum RevisionsView
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Original | `0` | يحدد الإصدار الأصلي للمستند. |
| Final | `1` | يحدد الإصدار المنقح للمستند. |

## أمثلة

يوضح كيفية التبديل بين العرض المنقح والعرض الأصلي للمستند.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// عرض كائن المستند كما لو أن جميع المراجعات مقبولة. يدعم حاليًا تسميات القوائم.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
