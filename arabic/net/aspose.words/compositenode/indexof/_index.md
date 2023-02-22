---
title: CompositeNode.IndexOf
second_title: Aspose.Words لمراجع .NET API
description: CompositeNode طريقة. إرجاع فهرس العقدة الفرعية المحددة في مصفوفة العقدة الفرعية.
type: docs
weight: 130
url: /ar/net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

إرجاع فهرس العقدة الفرعية المحددة في مصفوفة العقدة الفرعية.

```csharp
public int IndexOf(Node child)
```

### ملاحظات

إرجاع -1 إذا لم يتم العثور على العقدة في العقد الفرعية.

### أمثلة

يوضح كيفية الحصول على فهرس عقدة فرعية معينة من أصلها.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

Body body = doc.FirstSection.Body;

// استرجع فهرس الفقرة الأخيرة في نص القسم الأول.
Assert.AreEqual(24, body.ChildNodes.IndexOf(body.LastParagraph));
```

### أنظر أيضا

* class [Node](../../node/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../compositenode/)
* المجسم [Aspose.Words](../../../)


