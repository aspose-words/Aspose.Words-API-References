---
title: Node.Document
second_title: Aspose.Words لمراجع .NET API
description: Node ملكية. الحصول على المستند الذي تنتمي إليه هذه العقدة.
type: docs
weight: 20
url: /ar/net/aspose.words/node/document/
---
## Node.Document property

الحصول على المستند الذي تنتمي إليه هذه العقدة.

```csharp
public virtual DocumentBase Document { get; }
```

### ملاحظات

تنتمي العقدة دائمًا إلى مستند حتى لو تم إنشاؤه للتو ولم تتم إضافته بعد إلى الشجرة، أو إذا تمت إزالته من الشجرة.

### أمثلة

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

* class [DocumentBase](../../documentbase/)
* class [Node](../)
* مساحة الاسم [Aspose.Words](../../node/)
* المجسم [Aspose.Words](../../../)


