---
title: "طريقة Aspose::Words::DocumentBuilder::MoveToBookmark"
linktitle: "MoveToBookmark"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::MoveToBookmark. ينقل المؤشر إلى علامة مرجعية في C++."
type: docs
weight: 52000
url: /ar/cpp/aspose.words/documentbuilder/movetobookmark/
---
## DocumentBuilder::MoveToBookmark(const System::String\&) method


ينقل المؤشر إلى إشارة مرجعية.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| bookmarkName | const System::String\& | اسم العلامة المرجعية التي يُنقل المؤشر إليها. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## ملاحظات


ينقل المؤشر إلى موضع مباشرة بعد بداية العلامة المرجعية ذات الاسم المحدد.

المقارنة غير حساسة لحالة الأحرف. إذا لم يتم العثور على العلامة المرجعية، يتم إرجاع **false** ولا يتم نقل المؤشر.

Inserting new text does not replace existing text of the bookmark.

لاحظ أن بعض الإشارات المرجعية في المستند مخصصة لحقول النماذج. الانتقال إلى مثل هذه الإشارة المرجعية وإدراج نص هناك يضيف النص إلى شفرة حقل النموذج. على الرغم من أن ذلك لن يبطل حقل النموذج، إلا أن النص المدخل لن يكون مرئياً لأنه يصبح جزءاً من شفرة الحقل.

## أمثلة



يوضح كيفية نقل مؤشر منشئ المستند إلى عقد مختلفة في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء إشارة مرجعية صالحة، كيان يتكون من عقد محاطة بعقدة بداية الإشارة المرجعية،
// وعقدة نهاية الإشارة المرجعية.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Bookmark contents.");
builder->EndBookmark(u"MyBookmark");

System::SharedPtr<Aspose::Words::NodeCollection> firstParagraphNodes = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, firstParagraphNodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Run, firstParagraphNodes->idx_get(1)->get_NodeType());
ASSERT_EQ(u"Bookmark contents.", firstParagraphNodes->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::NodeType::BookmarkEnd, firstParagraphNodes->idx_get(2)->get_NodeType());

// مؤشر منشئ المستند يكون دائمًا أمام العقدة التي أضفناها آخرًا باستخدامه.
// إذا كان مؤشر المنشئ في نهاية المستند، فستكون العقدة الحالية له null.
// العقدة السابقة هي عقدة نهاية الإشارة المرجعية التي أضفناها آخرًا.
// إضافة عقد جديدة باستخدام المنشئ سيُضيفها إلى العقدة الأخيرة.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// إذا رغبنا في تعديل جزء مختلف من المستند باستخدام المنشئ،
// سنحتاج إلى جلب المؤشر إلى العقدة التي نرغب في تعديلها.
builder->MoveToBookmark(u"MyBookmark");

// نقله إلى إشارة مرجعية سيحركه إلى أول عقدة داخل عقد بداية ونهاية الإشارة المرجعية، وهو النص المتضمن.
ASPOSE_ASSERT_EQ(firstParagraphNodes->idx_get(1), builder->get_CurrentNode());

// يمكننا أيضًا نقل المؤشر إلى عقدة فردية بهذه الطريقة.
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false)->idx_get(0));

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, builder->get_CurrentNode()->get_NodeType());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), builder->get_CurrentParagraph());
ASSERT_TRUE(builder->get_IsAtStartOfParagraph());

// يمكننا استخدام طرق محددة للانتقال إلى بداية/نهاية المستند.
builder->MoveToDocumentEnd();

ASSERT_TRUE(builder->get_IsAtEndOfParagraph());

builder->MoveToDocumentStart();

ASSERT_TRUE(builder->get_IsAtStartOfParagraph());
```

## انظر أيضًا

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToBookmark(const System::String\&, bool, bool) method


ينقل المؤشر إلى إشارة مرجعية بدقة أكبر.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName, bool isStart, bool isAfter)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| bookmarkName | const System::String\& | اسم العلامة المرجعية التي يُنقل المؤشر إليها. |
| isStart | bool | عند **true**، ينقل المؤشر إلى بداية الإشارة المرجعية. عند **false**، ينقل المؤشر إلى نهاية الإشارة المرجعية. |
| isAfter | bool | عند **true**، ينقل المؤشر ليكون بعد موضع بداية أو نهاية الإشارة المرجعية. عند **false**، ينقل المؤشر ليكون قبل موضع بداية أو نهاية الإشارة المرجعية. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## ملاحظات


ينقل المؤشر إلى موضع قبل أو بعد بداية أو نهاية الإشارة المرجعية.

إذا لم يكن الموضع المطلوب على مستوى السطر الداخلي، ينتقل إلى الفقرة التالية.

المقارنة غير حساسة لحالة الأحرف. إذا لم يتم العثور على العلامة المرجعية، يتم إرجاع **false** ولا يتم نقل المؤشر.

## أمثلة



يوضح كيفية نقل مؤشر نقطة إدراج العقدة في مُنشئ المستند إلى إشارة مرجعية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// الإشارة المرجعية الصالحة تتكون من عقدة BookmarkStart، وعقدة BookmarkEnd مع
// اسم إشارة مرجعية مطابق في مكان ما بعد ذلك، والمحتوى محاط بهذه العقد.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world! ");
builder->EndBookmark(u"MyBookmark");

// هناك 4 طرق لنقل مؤشر مُنشئ المستند إلى إشارة مرجعية.
// إذا كنا بين عقدتي BookmarkStart وBookmarkEnd، سيكون المؤشر داخل الإشارة المرجعية.
// هذا يعني أن أي نص يضيفه المُنشئ سيصبح جزءاً من الإشارة المرجعية.
// 1 -  خارج الإشارة المرجعية، أمام عقدة BookmarkStart:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, false));
builder->Write(u"1. ");

ASSERT_EQ(u"Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. Hello world!", doc->GetText().Trim());

// 2 -  داخل الإشارة المرجعية، مباشرة بعد عقدة BookmarkStart:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, true));
builder->Write(u"2. ");

ASSERT_EQ(u"2. Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world!", doc->GetText().Trim());

// 2 -  داخل الإشارة المرجعية، مباشرة أمام عقدة BookmarkEnd:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, false));
builder->Write(u"3. ");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3.", doc->GetText().Trim());

// 4 -  خارج الإشارة المرجعية، بعد عقدة BookmarkEnd:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, true));
builder->Write(u"4.");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3. 4.", doc->GetText().Trim());
```

## انظر أيضًا

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
