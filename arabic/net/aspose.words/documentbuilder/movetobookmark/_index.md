---
title: DocumentBuilder.MoveToBookmark
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. ينقل المؤشر إلى إشارة مرجعية .
type: docs
weight: 470
url: /ar/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(string) {#movetobookmark}

ينقل المؤشر إلى إشارة مرجعية .

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| bookmarkName | String | اسم الإشارة المرجعية المراد نقل المؤشر إليها. |

### قيمة الإرجاع

صحيح إذا تم العثور على الإشارة المرجعية ؛ خطأ خلاف ذلك.

### ملاحظات

ينقل المؤشر إلى موضع بعد بداية الإشارة المرجعية بالاسم المحدد .

المقارنة ليست حساسة لحالة الأحرف. إذا لم يتم العثور على الإشارة المرجعية ، فسيتم إرجاع خطأ is ولن يتم نقل المؤشر.

إدراج نص جديد لا يحل محل النص الموجود للإشارة المرجعية.

لاحظ أن بعض الإشارات المرجعية في المستند مخصصة لحقول النموذج. على الرغم من أن هذا لن يبطل حقل النموذج ، لن يكون النص المدرج مرئيًا لأنه يصبح جزءًا من رمز الحقل.

### أمثلة

يوضح كيفية نقل مؤشر منشئ المستندات إلى عقد مختلفة في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء إشارة مرجعية صالحة ، كيان يتكون من عقد محاطة بعقدة بدء إشارة مرجعية ،
 // وعقدة نهاية مرجعية.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.ChildNodes;

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// دائمًا ما يكون مؤشر منشئ المستندات متقدمًا على العقدة التي أضفناها بها آخر مرة.
// إذا كان مؤشر المنشئ في نهاية المستند ، فستكون العقدة الحالية خالية.
// العقدة السابقة هي نقطة نهاية الإشارة المرجعية التي أضفناها آخر مرة.
// ستؤدي إضافة عقد جديدة مع المنشئ إلى إلحاقها بالعقدة الأخيرة.
Assert.Null(builder.CurrentNode);

// إذا كنا نرغب في تحرير جزء مختلف من المستند باستخدام المنشئ ،
// سنحتاج إلى إحضار مؤشرها إلى العقدة التي نرغب في تعديلها.
builder.MoveToBookmark("MyBookmark");

// سيؤدي نقله إلى إشارة مرجعية إلى نقله إلى العقدة الأولى داخل عقد بداية ونهاية الإشارة المرجعية ، المسار المغلق.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// يمكننا أيضًا تحريك المؤشر إلى عقدة فردية مثل هذه.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// يمكننا استخدام طرق محددة للانتقال إلى بداية / نهاية المستند.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## MoveToBookmark(string, bool, bool) {#movetobookmark_1}

ينقل المؤشر إلى إشارة مرجعية بدقة أكبر .

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| bookmarkName | String | اسم الإشارة المرجعية المراد نقل المؤشر إليها. |
| isStart | Boolean | عندما يكون صحيحًا ، ينقل المؤشر إلى بداية الإشارة المرجعية . عندما يكون خطأً ، ينقل المؤشر إلى نهاية الإشارة المرجعية. |
| isAfter | Boolean | عندما يكون صحيحًا ، يحرك المؤشر ليكون بعد موضع البداية أو النهاية bookmark . عندما يكون خطأ ، يحرك المؤشر ليكون قبل bookmark موضع البداية أو النهاية. |

### قيمة الإرجاع

صحيح إذا تم العثور على الإشارة المرجعية ؛ خطأ خلاف ذلك.

### ملاحظات

ينقل المؤشر إلى موضع قبل أو بعد بداية الإشارة المرجعية أو نهايتها.

إذا لم يكن الموضع المطلوب في المستوى المضمن ، فانتقل إلى الفقرة التالية.

المقارنة ليست حساسة لحالة الأحرف. إذا لم يتم العثور على الإشارة المرجعية ، فسيتم إرجاع خطأ is ولن يتم نقل المؤشر.

### أمثلة

يوضح كيفية نقل مؤشر نقطة إدراج عقدة منشئ المستندات إلى إشارة مرجعية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تتكون الإشارة المرجعية الصالحة من عقدة BookmarkStart ، عقدة BookmarkEnd ذات ملف
// مطابقة اسم الإشارة المرجعية في مكان ما بعد ذلك ، والمحتويات المرفقة بهذه العقد.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// هناك 4 طرق لنقل مؤشر منشئ المستندات إلى إشارة مرجعية.
// إذا كنا بين عقدتي BookmarkStart و BookmarkEnd ، فسيكون المؤشر داخل الإشارة المرجعية.
// هذا يعني أن أي نص يضيفه المنشئ سيصبح جزءًا من الإشارة المرجعية.
// 1 - خارج الإشارة المرجعية ، أمام عقدة BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, false));
builder.Write("1. ");

Assert.AreEqual("Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. Hello world!", doc.GetText().Trim());

// 2 - داخل الإشارة المرجعية ، مباشرة بعد عقدة BookmarkStart:
Assert.True(builder.MoveToBookmark("MyBookmark", true, true));
builder.Write("2. ");

Assert.AreEqual("2. Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world!", doc.GetText().Trim());

// 2 - داخل الإشارة المرجعية ، أمام عقدة BookmarkEnd مباشرةً:
Assert.True(builder.MoveToBookmark("MyBookmark", false, false));
builder.Write("3. ");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3.", doc.GetText().Trim());

// 4 - خارج الإشارة المرجعية ، بعد عقدة BookmarkEnd:
Assert.True(builder.MoveToBookmark("MyBookmark", false, true));
builder.Write("4.");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3. 4.", doc.GetText().Trim());
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


