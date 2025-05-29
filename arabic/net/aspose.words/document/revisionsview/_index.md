---
title: Document.RevisionsView
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words لـ .NET
description: أدر مراجعات المستندات بسهولة! اختر بين الإصدارات الأصلية أو المُحدّثة لتعاون سلس وإنتاجية مُحسّنة.
type: docs
weight: 380
url: /ar/net/aspose.words/document/revisionsview/
---
## Document.RevisionsView property

يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان سيتم العمل مع الإصدار الأصلي أو المنقح للمستند.

```csharp
public RevisionsView RevisionsView { get; set; }
```

## ملاحظات

القيمة الافتراضية هي .

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

* enum [RevisionsView](../../revisionsview/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
