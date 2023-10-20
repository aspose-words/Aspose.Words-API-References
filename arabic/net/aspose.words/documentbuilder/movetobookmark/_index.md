---
title: DocumentBuilder.MoveToBookmark
linktitle: MoveToBookmark
articleTitle: MoveToBookmark
second_title: Aspose.Words لـ .NET
description: DocumentBuilder MoveToBookmark طريقة. ينقل المؤشر إلى إشارة مرجعية في C#.
type: docs
weight: 490
url: /ar/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(*string*) {#movetobookmark}

ينقل المؤشر إلى إشارة مرجعية.

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| bookmarkName | String | اسم الإشارة المرجعية التي سيتم تحريك المؤشر إليها. |

### قيمة الإرجاع

`حقيقي` إذا تم العثور على الإشارة المرجعية؛`خطأ شنيع` خلاف ذلك.

## ملاحظات

يحرك المؤشر إلى موضع بعد بداية الإشارة المرجعية بالاسم المحدد .

المقارنة ليست حساسة لحالة الأحرف. إذا لم يتم العثور على الإشارة المرجعية،`خطأ شنيع` تم إرجاع is ولم يتم تحريك المؤشر.

لا يؤدي إدراج نص جديد إلى استبدال النص الموجود للإشارة المرجعية.

لاحظ أنه تم تعيين بعض الإشارات المرجعية في المستند لحقول النموذج. الانتقال إلى مثل هذه الإشارة المرجعية وإدراج نص هناك يؤدي إلى إدراج النص في رمز حقل النموذج . على الرغم من أن هذا لن يؤدي إلى إبطال حقل النموذج، إلا أن النص المدرج لن يكون مرئيًا لأنه يصبح جزءًا من رمز الحقل.

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

---

## MoveToBookmark(*string, bool, bool*) {#movetobookmark_1}

ينقل المؤشر إلى إشارة مرجعية بدقة أكبر.

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| bookmarkName | String | اسم الإشارة المرجعية التي سيتم تحريك المؤشر إليها. |
| isStart | Boolean | متى`حقيقي` ، يحرك المؤشر إلى بداية الإشارة المرجعية. متى`خطأ شنيع`، يحرك المؤشر إلى نهاية الإشارة المرجعية. |
| isAfter | Boolean | متى`حقيقي` ، يحرك المؤشر ليكون بعد موضع البداية أو النهاية للإشارة المرجعية . متى`خطأ شنيع`، يحرك المؤشر ليكون قبل موضع البداية أو النهاية للإشارة المرجعية . |

### قيمة الإرجاع

`حقيقي` إذا تم العثور على الإشارة المرجعية؛`خطأ شنيع` خلاف ذلك.

## ملاحظات

يحرك المؤشر إلى موضع قبل أو بعد بداية الإشارة المرجعية أو نهايتها.

إذا لم يكن الموضع المطلوب على المستوى السطري، فانتقل إلى الفقرة التالية.

المقارنة ليست حساسة لحالة الأحرف. إذا لم يتم العثور على الإشارة المرجعية،`خطأ شنيع` تم إرجاع is ولم يتم تحريك المؤشر.

## أمثلة

يوضح كيفية نقل مؤشر نقطة إدراج عقدة أداة إنشاء المستندات إلى إشارة مرجعية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تتكون الإشارة المرجعية الصالحة من عقدة BookmarkStart، وعقدة BookmarkEnd مع a
// مطابقة اسم الإشارة المرجعية في مكان ما بعد ذلك، والمحتويات المحاطة بتلك العقد.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// هناك أربع طرق لتحريك مؤشر أداة إنشاء المستندات إلى إشارة مرجعية.
// إذا كنا بين عقدتي BookmarkStart وBookmarkEnd، فسيكون المؤشر داخل الإشارة المرجعية.
// هذا يعني أن أي نص يضيفه المنشئ سيصبح جزءًا من الإشارة المرجعية.
// 1 - خارج الإشارة المرجعية، أمام عقدة BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, false));
builder.Write("1. ");

Assert.AreEqual("Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. Hello world!", doc.GetText().Trim());

// 2 - داخل الإشارة المرجعية، مباشرة بعد عقدة BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, true));
builder.Write("2. ");

Assert.AreEqual("2. Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world!", doc.GetText().Trim());

// 2 - داخل الإشارة المرجعية، مباشرة أمام عقدة BookmarkEnd:
Assert.True(builder.MoveToBookmark("MyBookmark", false, false));
builder.Write("3. ");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3.", doc.GetText().Trim());

// 4 - خارج الإشارة المرجعية، بعد عقدة BookmarkEnd:
Assert.True(builder.MoveToBookmark("MyBookmark", false, true));
builder.Write("4.");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3. 4.", doc.GetText().Trim());
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
