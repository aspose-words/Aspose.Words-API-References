---
title: RevisionsView Enum
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words لـ .NET
description: Aspose.Words.RevisionsView تعداد. يسمح بتحديد ما إذا كان سيتم العمل مع النسخة الأصلية أو المنقحة من المستند في C#.
type: docs
weight: 4810
url: /ar/net/aspose.words/revisionsview/
---
## RevisionsView enumeration

يسمح بتحديد ما إذا كان سيتم العمل مع النسخة الأصلية أو المنقحة من المستند.

```csharp
public enum RevisionsView
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Original | `0` | يحدد النسخة الأصلية للمستند. |
| Final | `1` | يحدد النسخة المنقحة من المستند. |

## أمثلة

يوضح كيفية التبديل بين العرض الأصلي والمراجع للمستند.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// اعرض كائن المستند كما لو تم قبول جميع المراجعات. يدعم حاليا تسميات القائمة.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
