---
title: DocumentBuilder.MoveTo
linktitle: MoveTo
articleTitle: MoveTo
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة MoveTo في DocumentBuilder للتنقل بسهولة بين العقد المضمنة ووضع المؤشر بكفاءة في نهايات الفقرات لتحرير المستندات بسلاسة.
type: docs
weight: 520
url: /ar/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

يحرك المؤشر إلى عقدة مضمنة أو إلى نهاية فقرة.

```csharp
public void MoveTo(Node node)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| node | Node | يجب أن تكون العقدة فقرة أو فرعًا مباشرًا لفقرة. |

## ملاحظات

متىالعقدة هي عقدة على مستوى الخط، يتم نقل المؤشر إلى هذه العقدة وسيتم إدراج المزيد من المحتوى قبل تلك العقدة.

متىالعقدة هو[`Paragraph`](../../paragraph/)، يتم نقل المؤشر إلى نهاية الفقرة وسيتم إدراج المزيد من المحتوى قبل فاصل الفقرة مباشرةً.

متىالعقدة هي عقدة على مستوى الكتلة ولكنها ليست[`Paragraph`](../../paragraph/)، يتم نقل المؤشر إلى نهاية الفقرة الأولى في node على مستوى الكتلة وسيتم إدراج المزيد من المحتوى قبل فاصل الفقرة مباشرةً.

## أمثلة

يوضح كيفية نقل موضع مؤشر DocumentBuilder إلى عقدة محددة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// يحتوي منشئ المستندات على مؤشر يعمل كجزء من المستند
// حيث يقوم المنشئ بإضافة عقد جديدة عندما نستخدم أساليب إنشاء المستندات الخاصة به.
// يعمل هذا المؤشر بنفس الطريقة التي يعمل بها المؤشر الوامض في برنامج Microsoft Word،
// وينتهي دائمًا على الفور بعد أي عقدة أدخلها المنشئ للتو.
// لإضافة محتوى إلى جزء مختلف من المستند،
// يمكننا نقل المؤشر إلى عقدة مختلفة باستخدام طريقة "MoveTo".
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// أصبح المؤشر الآن أمام العقدة التي نقلناه إليها.
// إضافة تشغيل ثانٍ سيؤدي إلى إدراجه أمام التشغيل الأول.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// حرك المؤشر إلى نهاية المستند لمواصلة إضافة النص إلى النهاية كما في السابق.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
