---
title: NodeCollection.Add
second_title: Aspose.Words لمراجع .NET API
description: NodeCollection طريقة. يضيف عقدة إلى نهاية المجموعة.
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
| node | Node | العقدة المراد إضافتها إلى نهاية المجموعة. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| NotSupportedException | ال **NodeCollection** هي مجموعة "عميقة". |

### ملاحظات

يتم إدراج العقدة كطفل في كائن العقدة الذي تم إنشاء المجموعة منه.

إذا كان الطفل الجديد موجودًا بالفعل في الشجرة ، فسيتم إزالته أولاً.

إذا تم إنشاء العقدة التي يتم إدراجها من مستند آخر ، فيجب عليك استخدام [`ImportNode`](../../documentbase/importnode/) لاستيراد العقدة إلى المستند الحالي. يمكن بعد ذلك إدراج العقدة المستوردة في المستند الحالي.

### أمثلة

يوضح كيفية تحضير عقدة قسم جديدة للتحرير.

```csharp
Document doc = new Document();

// يأتي المستند الفارغ مع قسم يحتوي على نص ، والذي بدوره يحتوي على فقرة.
// يمكننا إضافة محتويات إلى هذا المستند عن طريق إضافة عناصر مثل عمليات تشغيل النص أو الأشكال أو الجداول إلى تلك الفقرة.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// إذا أضفنا قسمًا جديدًا مثل هذا ، فلن يحتوي على جسم ، أو أي عقد فرعية أخرى.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// قم بتشغيل طريقة "ضمان الحد الأدنى" لإضافة نص وفقرة إلى هذا القسم لبدء تحريره.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* class [Node](../../node/)
* class [NodeCollection](../)
* مساحة الاسم [Aspose.Words](../../nodecollection/)
* المجسم [Aspose.Words](../../../)


