---
title: Section.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words لـ .NET
description: قم بتحسين المحتوى الخاص بك باستخدام طريقة EnsureMinimum، مما يضمن أن يتضمن كل قسم نصًا مع فقرة لتحسين الوضوح والبنية.
type: docs
weight: 150
url: /ar/net/aspose.words/section/ensureminimum/
---
## Section.EnsureMinimum method

يتأكد من أن القسم يحتوي على[`Body`](../body/) مع واحد[`Paragraph`](../../paragraph/) .

```csharp
public void EnsureMinimum()
```

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

* class [Section](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
