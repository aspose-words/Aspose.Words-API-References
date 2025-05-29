---
title: DocumentBuilder.MoveToBookmark
linktitle: MoveToBookmark
articleTitle: MoveToBookmark
second_title: Aspose.Words لـ .NET
description: قم بالتنقل بسهولة عبر مستنداتك باستخدام طريقة MoveToBookmark في DocumentBuilder، مما يؤدي إلى وضع المؤشر على الفور في أي إشارة مرجعية لتحسين التحرير.
type: docs
weight: 530
url: /ar/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(*string*) {#movetobookmark}

يحرك المؤشر إلى الإشارة المرجعية.

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| bookmarkName | String | اسم الإشارة المرجعية التي سيتم نقل المؤشر إليها. |

### قيمة الإرجاع

`حقيقي` إذا تم العثور على الإشارة المرجعية؛`خطأ شنيع` خلاف ذلك.

## ملاحظات

يحرك المؤشر إلى موضع بعد بداية الإشارة المرجعية بالاسم المحدد .

المقارنة لا تراعي حالة الأحرف. إذا لم يتم العثور على الإشارة المرجعية،`خطأ شنيع` تم إرجاع is ولم يتم تحريك المؤشر.

إن إدراج نص جديد لا يحل محل النص الموجود في الإشارة المرجعية.

لاحظ أن بعض الإشارات المرجعية في المستند مُخصصة لحقول النماذج. يؤدي الانتقال إلى هذه الإشارة المرجعية وإدراج نص فيها إلى إدراج النص في رمز حقل النموذج . مع أن هذا لن يُبطل حقل النموذج، إلا أن النص المُدرج لن يكون مرئيًا لأنه سيصبح جزءًا من رمز الحقل.

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

---

## MoveToBookmark(*string, bool, bool*) {#movetobookmark_1}

يحرك المؤشر إلى إشارة مرجعية بدقة أكبر.

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| bookmarkName | String | اسم الإشارة المرجعية التي سيتم نقل المؤشر إليها. |
| isStart | Boolean | متى`حقيقي` ، يحرك المؤشر إلى بداية الإشارة المرجعية. عندما`خطأ شنيع`، يحرك المؤشر إلى نهاية الإشارة المرجعية. |
| isAfter | Boolean | متى`حقيقي` ، يحرك المؤشر ليكون بعد موضع البداية أو النهاية bookmark . عندما`خطأ شنيع`، يحرك المؤشر ليكون قبل موضع البداية أو النهاية bookmark . |

### قيمة الإرجاع

`حقيقي` إذا تم العثور على الإشارة المرجعية؛`خطأ شنيع` خلاف ذلك.

## ملاحظات

يحرك المؤشر إلى موضع قبل أو بعد بداية أو نهاية الإشارة المرجعية.

إذا لم يكن الموضع المطلوب على مستوى الخط، يتم الانتقال إلى الفقرة التالية.

المقارنة لا تراعي حالة الأحرف. إذا لم يتم العثور على الإشارة المرجعية،`خطأ شنيع` تم إرجاع is ولم يتم تحريك المؤشر.

## أمثلة

يوضح كيفية نقل مؤشر نقطة إدراج عقدة منشئ المستندات إلى إشارة مرجعية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تتكون الإشارة المرجعية الصالحة من عقدة BookmarkStart وعقدة BookmarkEnd مع
// مطابقة اسم الإشارة المرجعية في مكان ما بعد ذلك، والمحتويات المحيطة بتلك العقد.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// هناك 4 طرق لنقل مؤشر منشئ المستندات إلى الإشارة المرجعية.
// إذا كنا بين عقدتي BookmarkStart وBookmarkEnd، فسيكون المؤشر داخل الإشارة المرجعية.
// وهذا يعني أن أي نص تمت إضافته بواسطة المنشئ سيصبح جزءًا من الإشارة المرجعية.
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
