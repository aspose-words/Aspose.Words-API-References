---
title: Node.ParentNode
linktitle: ParentNode
articleTitle: ParentNode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Node ParentNode للوصول بسهولة إلى الوالد المباشر لأي عقدة، مما يعزز كفاءة تطوير الويب ووضوح الكود.
type: docs
weight: 60
url: /ar/net/aspose.words/node/parentnode/
---
## Node.ParentNode property

يحصل على الوالد المباشر لهذه العقدة.

```csharp
public CompositeNode ParentNode { get; }
```

## ملاحظات

إذا تم إنشاء عقدة للتو ولم تتم إضافتها إلى الشجرة بعد، أو إذا تمت إزالتها من الشجرة، فإن العقدة الأصلية هي`باطل`.

## أمثلة

يوضح كيفية الوصول إلى العقدة الأصلية للعقدة.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// أضف عقدة تشغيل فرعية إلى الفقرة الأولى من المستند.
Run run = new Run(doc, "Hello world!");
para.AppendChild(run);

// الفقرة هي العقدة الأم لعقدة التشغيل. يمكننا تتبع هذا النسب.
// كل الطريق إلى عقدة المستند، والتي هي جذر شجرة عقد المستند.
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

// لم نقم بعد بإضافة هذه الفقرة كفقرة فرعية إلى أي عقدة مركبة.
Assert.IsNull(para.ParentNode);

// إذا كانت العقدة هي نوع عقدة فرعية مناسب لعقدة مركبة أخرى،
// يمكننا إرفاقه كطفل فقط إذا كان لدى كلتا العقدتين نفس مستند المالك.
//مستند المالك هو المستند الذي مررناه إلى منشئ العقدة.
// لم نقم بإرفاق هذه الفقرة بالمستند، وبالتالي فإن المستند لا يحتوي على نصها.
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// بما أن المستند يمتلك هذه الفقرة، فيمكننا تطبيق أحد أنماطه على محتويات الفقرة.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

//أضف هذه العقدة إلى المستند، ثم تحقق من محتوياته.
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
