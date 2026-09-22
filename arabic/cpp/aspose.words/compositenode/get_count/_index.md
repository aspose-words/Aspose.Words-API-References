---
title: "طريقة Aspose::Words::CompositeNode::get_Count"
linktitle: "get_Count"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::CompositeNode::get_Count. يحصل على عدد الأطفال المباشرين لهذه العقدة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/compositenode/get_count/
---
## CompositeNode::get_Count method


يحصل على عدد الأطفال المباشرين لهذه العقدة.

```cpp
int32_t Aspose::Words::CompositeNode::get_Count()
```


## أمثلة



يوضح كيفية إضافة وتحديث وحذف العقد الفرعية في مجموعة الأطفال لـ [CompositeNode](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// المستند الفارغ، بشكل افتراضي، يحتوي على فقرة واحدة.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// العقد المركبة مثل فقرتنا يمكنها احتواء عقد مركبة أخرى وعقد داخلية كعناصر فرعية.
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// أنشئ ثلاث عقد تشغيل إضافية.
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// لن يعرض جسم المستند هذه المقاطع حتى نقوم بإدراجها في عقدة مركبة
// التي هي نفسها جزء من شجرة عقد المستند، كما فعلنا مع المقطع الأول.
// يمكننا تحديد أين تظهر محتويات النص للعقد التي نقوم بإدراجها
// تظهر في المستند عن طريق تحديد موقع الإدراج بالنسبة لعقدة أخرى في الفقرة.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// أدرج المقطع الثاني في الفقرة أمام المقطع الأول.
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// أدرج المقطع الثالث بعد المقطع الأول.
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// أدرج المقطع الأول في بداية مجموعة العقد الفرعية للفقرة.
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// يمكننا تعديل محتويات المقطع عن طريق تحرير وحذف العقد الفرعية الموجودة.
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```

## انظر أيضًا

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
