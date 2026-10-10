---
title: "طريقة Aspose::Words::Node::get_ParentNode"
linktitle: "get_ParentNode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Node::get_ParentNode. يحصل على الوالد الفوري لهذه العقدة في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words/node/get_parentnode/
---
## Node::get_ParentNode method


يحصل على الوالد المباشر لهذه العقدة.

```cpp
System::SharedPtr<Aspose::Words::CompositeNode> Aspose::Words::Node::get_ParentNode()
```

## ملاحظات


إذا تم إنشاء عقدة للتو ولم تُضاف بعد إلى الشجرة، أو إذا أُزيلت من الشجرة، فإن الوالد هو **null**.

## أمثلة



يوضح كيفية الوصول إلى عقدة الوالد لعقدة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// إلحاق عقدة Run فرعية إلى الفقرة الأولى في المستند.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// الفقرة هي عقدة الوالد لعقدة الـ Run. يمكننا تتبع هذا النسب
// حتى عقدة المستند، التي هي جذر شجرة عقد المستند.
ASPOSE_ASSERT_EQ(para, run->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection(), doc->get_FirstSection()->get_Body()->get_ParentNode());
ASPOSE_ASSERT_EQ(doc, doc->get_FirstSection()->get_ParentNode());
```


يوضح كيفية إنشاء عقدة وتعيين المستند المالك لها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// لم نقم بعد بإلحاق هذه الفقرة كطفل إلى أي عقدة مركبة.
ASSERT_TRUE(System::TestTools::IsNull(para->get_ParentNode()));

// إذا كانت العقدة نوعًا مناسبًا من العقد الفرعية لعقدة مركبة أخرى،
// يمكننا إرفاقها كطفل فقط إذا كان لدى كلتا العقدتين نفس المستند المالك.
// المستند المالك هو المستند الذي مررناه إلى مُنشئ العقدة.
// لم نقم بإرفاق هذه الفقرة إلى المستند، لذا لا يحتوي المستند على نصها.
ASPOSE_ASSERT_EQ(para->get_Document(), doc);
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());

// نظرًا لأن المستند يملك هذه الفقرة، يمكننا تطبيق أحد أنماطه على محتويات الفقرة.
para->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));

// أضف هذه العقدة إلى المستند، ثم تحقق من محتوياتها.
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## انظر أيضًا

* Class [CompositeNode](../../compositenode/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
