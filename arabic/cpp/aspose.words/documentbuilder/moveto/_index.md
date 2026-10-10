---
title: "Aspose::Words::DocumentBuilder::MoveTo method"
linktitle: "MoveTo"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::MoveTo method. ينقل المؤشر إلى عقدة داخلية أو إلى نهاية فقرة في C++."
type: docs
weight: 51000
url: /ar/cpp/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder::MoveTo method


ينقل المؤشر إلى عقدة مضمنة أو إلى نهاية الفقرة.

```cpp
void Aspose::Words::DocumentBuilder::MoveTo(const System::SharedPtr<Aspose::Words::Node> &node)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| node | const System::SharedPtr\<Aspose::Words::Node\>\& | يجب أن تكون العقدة فقرة أو طفلاً مباشراً لفقرة. |
## ملاحظات


عندما تكون *node* عقدة من المستوى الداخلي، يتم نقل المؤشر إلى هذه العقدة وسيتم إدراج المحتوى اللاحق قبل تلك العقدة.

عندما تكون *node* عبارة عن [Paragraph](../../paragraph/)، يتم نقل المؤشر إلى نهاية الفقرة وسيتم إدراج المحتوى اللاحق مباشرةً قبل فاصل الفقرة.

عندما تكون *node* عقدة على مستوى الكتلة ولكنها ليست [Paragraph](../../paragraph/)، يتم نقل المؤشر إلى نهاية الفقرة الأولى داخل عقدة مستوى الكتلة وسيتم إدراج المحتوى اللاحق مباشرةً قبل فاصل الفقرة.

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


يوضح كيفية نقل موضع مؤشر [DocumentBuilder](../) إلى عقدة محددة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Run 1. ");

// يمتلك منشئ المستند مؤشرًا، يعمل كجزء من المستند
// حيث يضيف المنشئ عقدًا جديدة عندما نستخدم طرق بناء المستند الخاصة به.
// هذا المؤشر يعمل بنفس طريقة مؤشر مايكروسوفت وورد الوميضي،
// وهو أيضًا **دائمًا** ينتهي **بعد** أي **عقدة** قام المنشئ بإدراجها للتو.
// لإضافة محتوى إلى جزء مختلف من المستند،
// يمكننا نقل المؤشر إلى عقدة مختلفة باستخدام طريقة "MoveTo".
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

// المؤشر الآن أمام العقدة التي نقلناه إليها.
// إضافة تشغيل ثانٍ سيُدرجه أمام التشغيل الأول.
builder->Writeln(u"Run 2. ");

ASSERT_EQ(u"Run 2. \rRun 1.", doc->GetText().Trim());

// انقل المؤشر إلى نهاية المستند لمتابعة إضافة النص إلى النهاية كما كان من قبل.
builder->MoveTo(doc->get_LastSection()->get_Body()->get_LastParagraph());
builder->Writeln(u"Run 3. ");

ASSERT_EQ(u"Run 2. \rRun 1. \rRun 3.", doc->GetText().Trim());
```

## انظر أيضًا

* Class [Node](../../node/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
