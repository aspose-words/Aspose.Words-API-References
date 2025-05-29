---
title: DocumentBuilder.IsAtStartOfParagraph
linktitle: IsAtStartOfParagraph
articleTitle: IsAtStartOfParagraph
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IsAtStartOfParagraph في DocumentBuilder. تحقق بسهولة من وجود المؤشر في بداية الفقرة لتحرير نصوص فعّال.
type: docs
weight: 130
url: /ar/net/aspose.words/documentbuilder/isatstartofparagraph/
---
## DocumentBuilder.IsAtStartOfParagraph property

إرجاع`حقيقي`إذا كان المؤشر في بداية الفقرة الحالية (لا يوجد نص قبل المؤشر).

```csharp
public bool IsAtStartOfParagraph { get; }
```

## أمثلة

يوضح كيفية نقل مؤشر منشئ المستندات إلى عقد مختلفة في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء إشارة مرجعية صالحة، وهي كيان يتكون من عقد محاطة بعقدة بداية الإشارة المرجعية،
 // وعقدة نهاية الإشارة المرجعية.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// يكون مؤشر منشئ المستند دائمًا أمام العقدة التي أضفناها معه آخر مرة.
// إذا كان مؤشر المنشئ في نهاية المستند، فستكون العقدة الحالية فارغة.
// العقدة السابقة هي عقدة نهاية الإشارة المرجعية التي أضفناها آخر مرة.
// إضافة عقد جديدة باستخدام المنشئ سوف يضيفها إلى العقدة الأخيرة.
Assert.Null(builder.CurrentNode);

// إذا أردنا تحرير جزء مختلف من المستند باستخدام المنشئ،
// سوف نحتاج إلى إحضار المؤشر إلى العقدة التي نرغب في تحريرها.
builder.MoveToBookmark("MyBookmark");

// نقله إلى إشارة مرجعية سوف ينقله إلى العقدة الأولى داخل عقدة بداية ونهاية الإشارة المرجعية، التشغيل المرفق.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

//يمكننا أيضًا نقل المؤشر إلى عقدة فردية مثل هذه.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

//يمكننا استخدام طرق محددة للانتقال إلى بداية/نهاية المستند.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
