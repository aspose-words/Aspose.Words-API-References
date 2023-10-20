---
title: CompositeNode.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words لـ .NET
description: CompositeNode IndexOf طريقة. إرجاع فهرس العقدة الفرعية المحددة في صفيف العقدة الفرعية في C#.
type: docs
weight: 120
url: /ar/net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

إرجاع فهرس العقدة الفرعية المحددة في صفيف العقدة الفرعية.

```csharp
public int IndexOf(Node child)
```

## ملاحظات

يُرجع -1 إذا لم يتم العثور على العقدة في العقد الفرعية.

## أمثلة

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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
