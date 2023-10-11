---
title: CompositeNode.IndexOf
second_title: Aspose.Words لمراجع .NET API
description: CompositeNode طريقة. إرجاع فهرس العقدة الفرعية المحددة في صفيف العقدة الفرعية.
type: docs
weight: 140
url: /ar/net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

إرجاع فهرس العقدة الفرعية المحددة في صفيف العقدة الفرعية.

```csharp
public int IndexOf(Node child)
```

### ملاحظات

يُرجع -1 إذا لم يتم العثور على العقدة في العقد الفرعية.

### أمثلة

يوضح كيفية الحصول على فهرس عقدة فرعية معينة من العقدة الأم.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

Body body = doc.FirstSection.Body;

// استرداد فهرس الفقرة الأخيرة في نص القسم الأول.
Assert.AreEqual(24, body.GetChildNodes(NodeType.Any, false).IndexOf(body.LastParagraph));
```

### أنظر أيضا

* class [Node](../../node/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../compositenode/)
* المجسم [Aspose.Words](../../../)


