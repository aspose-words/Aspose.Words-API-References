---
title: NodeCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة NodeCollection Add لإضافة العقد إلى مجموعتك بسهولة، مما يعزز إدارة البيانات لديك بسهولة وكفاءة.
type: docs
weight: 30
url: /ar/net/aspose.words/nodecollection/add/
---
## NodeCollection.Add method

يضيف عقدة إلى نهاية المجموعة.

```csharp
public void Add(Node node)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| node | Node | العقدة التي سيتم إضافتها إلى نهاية المجموعة. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| NotSupportedException | ال[`NodeCollection`](../) هي مجموعة "عميقة". |

## ملاحظات

يتم إدراج العقدة كطفل في كائن العقدة الذي تم إنشاء المجموعة منه.

إذا تم إنشاء العقدة التي يتم إدراجها من مستند آخر، فيجب عليك استخدام [`ImportNode`](../../documentbase/importnode/) لاستيراد العقدة إلى المستند الحالي. يمكن بعد ذلك إدراج العقدة المستوردة في المستند الحالي.

## أمثلة

يوضح كيفية إعداد عقدة قسم جديدة للتحرير.

```csharp
Document doc = new Document();

// تحتوي الوثيقة الفارغة على قسم يحتوي على نص، والذي بدوره يحتوي على فقرة.
// يمكننا إضافة محتويات إلى هذا المستند عن طريق إضافة عناصر مثل النصوص أو الأشكال أو الجداول إلى تلك الفقرة.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// إذا أضفنا قسمًا جديدًا مثل هذا، فلن يحتوي على نص أو أي عقدة فرعية أخرى.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// قم بتشغيل طريقة "EnsureMinimum" لإضافة نص ونص إلى هذا القسم لبدء تحريره.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* class [Node](../../node/)
* class [NodeCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
