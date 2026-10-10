---
title: "Aspose::Words::DocumentBuilder::get_IsAtStartOfParagraph method"
linktitle: "get_IsAtStartOfParagraph"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::get_IsAtStartOfParagraph method. تُرجع صحيح إذا كان المؤشر في بداية الفقرة الحالية (لا يوجد نص قبل المؤشر) في C++."
type: docs
weight: 20000
url: /ar/cpp/aspose.words/documentbuilder/get_isatstartofparagraph/
---
## DocumentBuilder::get_IsAtStartOfParagraph method


يرجع **true** إذا كان المؤشر في بداية الفقرة الحالية (لا يوجد نص قبل المؤشر).

```cpp
bool Aspose::Words::DocumentBuilder::get_IsAtStartOfParagraph()
```


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
