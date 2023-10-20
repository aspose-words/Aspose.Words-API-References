---
title: Node.ParentNode
linktitle: ParentNode
articleTitle: ParentNode
second_title: Aspose.Words لـ .NET
description: Node ParentNode ملكية. يحصل على الأصل المباشر لهذه العقدة في C#.
type: docs
weight: 60
url: /ar/net/aspose.words/node/parentnode/
---
## Node.ParentNode property

يحصل على الأصل المباشر لهذه العقدة.

```csharp
public CompositeNode ParentNode { get; }
```

## ملاحظات

إذا تم إنشاء العقدة للتو ولم تتم إضافتها بعد إلى الشجرة، أو إذا تمت إزالتها من الشجرة، فإن الأصل هو`باطل`.

## أمثلة

يوضح كيفية الوصول إلى العقدة الأصلية للعقدة.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// إلحاق عقدة تشغيل فرعية بالفقرة الأولى من المستند.
Run run = new Run(doc, "Hello world!");
para.AppendChild(run);

// الفقرة هي العقدة الأصلية لعقدة التشغيل. يمكننا تتبع هذا النسب
// وصولاً إلى عقدة المستند، وهي جذر شجرة عقدة المستند.
Assert.AreEqual(para, run.ParentNode);
Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual(doc.FirstSection, doc.FirstSection.Body.ParentNode);
Assert.AreEqual(doc, doc.FirstSection.ParentNode);
```

يوضح كيفية إنشاء عقدة وتعيين المستند الخاص بها.

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// لم نقم بعد بإلحاق هذه الفقرة كطفل لأي عقدة مركبة.
Assert.IsNull(para.ParentNode);

// إذا كانت العقدة عبارة عن نوع عقدة فرعية مناسب لعقدة مركبة أخرى،
// لا يمكننا إرفاقها كطفل إلا إذا كانت كلا العقدتين لهما نفس مستند المالك.
// مستند المالك هو المستند الذي مررناه إلى مُنشئ العقدة.
// لم نقم بإرفاق هذه الفقرة بالمستند، لذلك لا تحتوي الوثيقة على نصها.
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// بما أن المستند يمتلك هذه الفقرة، فيمكننا تطبيق أحد أنماطها على محتويات الفقرة.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// أضف هذه العقدة إلى المستند، ثم تحقق من محتوياتها.
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
