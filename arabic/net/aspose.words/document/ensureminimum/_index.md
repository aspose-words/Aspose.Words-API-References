---
title: Document.EnsureMinimum
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. في حالة عدم احتواء المستند على أقسام  يتم إنشاء قسم واحد به فقرة واحدة.
type: docs
weight: 560
url: /ar/net/aspose.words/document/ensureminimum/
---
## Document.EnsureMinimum method

في حالة عدم احتواء المستند على أقسام ، يتم إنشاء قسم واحد به فقرة واحدة.

```csharp
public void EnsureMinimum()
```

### أمثلة

يوضح كيفية التأكد من احتواء المستند على الحد الأدنى من مجموعة العقد المطلوبة لتحرير محتوياته.

```csharp
// يحتوي المستند الذي تم إنشاؤه حديثًا على قسم فرعي واحد ، والذي يتضمن عنصرًا فرعيًا واحدًا وفقرة فرعية واحدة.
// يمكننا تحرير محتويات جسم المستند عن طريق إضافة عقد مثل Runs أو inline Shapes إلى تلك الفقرة.
Document doc = new Document();
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(doc, nodes[0].ParentNode);

Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(nodes[0], nodes[1].ParentNode);

Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);
Assert.AreEqual(nodes[1], nodes[2].ParentNode);

// هذه هي الحد الأدنى من مجموعة العقد التي نحتاجها حتى نتمكن من تحرير المستند.
// لن نتمكن بعد الآن من تحرير المستند إذا أزلنا أيًا منها.
doc.RemoveAllChildren();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);

// اتصل بهذه الطريقة للتأكد من أن المستند يحتوي على هذه العقد الثلاثة على الأقل حتى نتمكن من تحريره مرة أخرى.
doc.EnsureMinimum();

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);

((Paragraph)nodes[2]).Runs.Add(new Run(doc, "Hello world!"));
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


