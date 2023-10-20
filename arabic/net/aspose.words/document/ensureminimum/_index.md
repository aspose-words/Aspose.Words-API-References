---
title: Document.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words لـ .NET
description: Document EnsureMinimum طريقة. إذا كانت الوثيقة لا تحتوي على أقسام قم بإنشاء قسم واحد بفقرة واحدة في C#.
type: docs
weight: 580
url: /ar/net/aspose.words/document/ensureminimum/
---
## Document.EnsureMinimum method

إذا كانت الوثيقة لا تحتوي على أقسام، قم بإنشاء قسم واحد بفقرة واحدة.

```csharp
public void EnsureMinimum()
```

## أمثلة

يوضح كيفية التأكد من أن المستند يحتوي على الحد الأدنى من العقد المطلوبة لتحرير محتوياته.

```csharp
// يحتوي المستند الذي تم إنشاؤه حديثًا على قسم فرعي واحد، يتضمن نصًا فرعيًا واحدًا وفقرة فرعية واحدة.
// يمكننا تحرير محتويات نص المستند عن طريق إضافة عقد مثل Runs أو الأشكال المضمنة إلى تلك الفقرة.
Document doc = new Document();
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(doc, nodes[0].ParentNode);

Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(nodes[0], nodes[1].ParentNode);

Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);
Assert.AreEqual(nodes[1], nodes[2].ParentNode);

// هذا هو الحد الأدنى من العقد التي نحتاجها حتى نتمكن من تحرير المستند.
// لن نتمكن بعد الآن من تحرير المستند إذا قمنا بإزالة أي منها.
doc.RemoveAllChildren();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);

// اتصل بهذه الطريقة للتأكد من أن المستند يحتوي على تلك العقد الثلاث على الأقل حتى نتمكن من تحريره مرة أخرى.
doc.EnsureMinimum();

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);

((Paragraph)nodes[2]).Runs.Add(new Run(doc, "Hello world!"));
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
