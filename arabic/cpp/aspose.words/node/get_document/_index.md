---
title: "طريقة Aspose::Words::Node::get_Document"
linktitle: "get_Document"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Node::get_Document. يحصل على المستند الذي تنتمي إليه هذه العقدة في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/node/get_document/
---
## Node::get_Document method


يحصل على المستند الذي تنتمي إليه هذه العقدة.

```cpp
virtual System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::Node::get_Document() const
```

## ملاحظات


العقدة دائمًا تنتمي إلى مستند حتى إذا تم إنشاؤها للتو ولم تُضاف بعد إلى الشجرة، أو إذا تم إزالتها من الشجرة.

## أمثلة



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

* Class [DocumentBase](../../documentbase/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
