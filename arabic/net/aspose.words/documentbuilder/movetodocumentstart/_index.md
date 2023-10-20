---
title: DocumentBuilder.MoveToDocumentStart
linktitle: MoveToDocumentStart
articleTitle: MoveToDocumentStart
second_title: Aspose.Words لـ .NET
description: DocumentBuilder MoveToDocumentStart طريقة. ينقل المؤشر إلى بداية المستند في C#.
type: docs
weight: 520
url: /ar/net/aspose.words/documentbuilder/movetodocumentstart/
---
## DocumentBuilder.MoveToDocumentStart method

ينقل المؤشر إلى بداية المستند.

```csharp
public void MoveToDocumentStart()
```

## أمثلة

يوضح كيفية نقل مؤشر أداة إنشاء المستندات إلى عقد مختلفة في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء إشارة مرجعية صالحة، وهو كيان يتكون من العقد المحاطة بعقدة بداية الإشارة المرجعية،
 // وعقدة نهاية الإشارة المرجعية.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// يكون مؤشر أداة إنشاء المستندات دائمًا متقدمًا على العقدة التي أضفناها معها آخر مرة.
// إذا كان مؤشر المنشئ في نهاية المستند، فستكون العقدة الحالية فارغة.
// العقدة السابقة هي عقدة نهاية الإشارة المرجعية التي أضفناها آخر مرة.
// ستؤدي إضافة عقد جديدة مع المنشئ إلى إلحاقها بالعقدة الأخيرة.
Assert.Null(builder.CurrentNode);

// إذا أردنا تحرير جزء مختلف من المستند باستخدام المنشئ،
// سنحتاج إلى إحضار المؤشر إلى العقدة التي نرغب في تحريرها.
builder.MoveToBookmark("MyBookmark");

// سيؤدي نقلها إلى إشارة مرجعية إلى نقلها إلى العقدة الأولى داخل عقدتي بداية ونهاية الإشارة المرجعية، وهي العملية المرفقة.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// يمكننا أيضًا نقل المؤشر إلى عقدة فردية مثل هذه.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// يمكننا استخدام طرق محددة للانتقال إلى بداية/نهاية المستند.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
