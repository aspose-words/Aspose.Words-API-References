---
title: DocumentBuilder.MoveTo
linktitle: MoveTo
articleTitle: MoveTo
second_title: Aspose.Words لـ .NET
description: DocumentBuilder MoveTo طريقة. ينقل المؤشر إلى عقدة مضمنة أو إلى نهاية الفقرة في C#.
type: docs
weight: 480
url: /ar/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

ينقل المؤشر إلى عقدة مضمنة أو إلى نهاية الفقرة.

```csharp
public void MoveTo(Node node)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| node | Node | يجب أن تكون العقدة فقرة أو فرعًا مباشرًا للفقرة. |

## ملاحظات

متىالعقدة هي عقدة ذات مستوى مضمّن، ويتم نقل المؤشر إلى هذه العقدة وسيتم إدراج محتوى إضافي قبل تلك العقدة.

متىالعقدة هو[`Paragraph`](../../paragraph/)، يتم نقل المؤشر إلى نهاية الفقرة وسيتم إدراج محتوى إضافي قبل فاصل الفقرة مباشرة.

متىالعقدة هي عقدة على مستوى الكتلة ولكنها ليست عقدة[`Paragraph`](../../paragraph/)، يتم نقل المؤشر إلى نهاية الفقرة الأولى إلى مستوى الكتلة العقدة وسيتم إدراج محتوى إضافي قبل فاصل الفقرة مباشرة.

## أمثلة

يوضح كيفية نقل موضع مؤشر DocumentBuilder إلى عقدة محددة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// يحتوي منشئ المستندات على مؤشر يعمل كجزء من المستند
// حيث يقوم المنشئ بإلحاق عقد جديدة عندما نستخدم طرق إنشاء المستندات الخاصة به.
// يعمل هذا المؤشر بنفس طريقة عمل المؤشر الوامض في Microsoft Word،
// وينتهي أيضًا دائمًا مباشرة بعد أي عقدة قام المنشئ بإدراجها للتو.
// لإلحاق محتوى بجزء مختلف من المستند،
// يمكننا نقل المؤشر إلى عقدة مختلفة باستخدام طريقة "MoveTo".
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// المؤشر الآن أمام العقدة التي نقلناه إليها.
// إضافة تشغيل ثانٍ سيؤدي إلى إدراجه أمام التشغيل الأول.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// حرك المؤشر إلى نهاية المستند لمواصلة إلحاق النص بالنهاية كما كان من قبل.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
