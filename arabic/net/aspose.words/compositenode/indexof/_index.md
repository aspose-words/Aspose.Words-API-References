---
title: CompositeNode.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم طريقة CompositeNode IndexOf بتحديد مؤشر عقدة فرعية محددة في المصفوفة بكفاءة، مما يعزز تجربة الترميز الخاصة بك.
type: docs
weight: 140
url: /ar/net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

يعيد مؤشر العقدة الفرعية المحددة في مجموعة العقد الفرعية.

```csharp
public int IndexOf(Node child)
```

## ملاحظات

يعود -1 إذا لم يتم العثور على العقدة في العقد الفرعية.

## أمثلة

يوضح كيفية الحصول على مؤشر عقدة فرعية معينة من عقدتها الأصلية.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

Body body = doc.FirstSection.Body;

//استرجاع فهرس الفقرة الأخيرة في نص القسم الأول.
Assert.AreEqual(24, body.GetChildNodes(NodeType.Any, false).IndexOf(body.LastParagraph));
```

### أنظر أيضا

* class [Node](../../node/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
