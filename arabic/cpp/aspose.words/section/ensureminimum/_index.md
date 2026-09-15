---
title: "طريقة Aspose::Words::Section::EnsureMinimum"
linktitle: "EnsureMinimum"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Section::EnsureMinimum. تضمن أن يحتوي القسم على Body مع فقرة واحدة في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/section/ensureminimum/
---
## Section::EnsureMinimum method


تضمن أن يحتوي القسم على [Body](../get_body/) مع فقرة واحدة [Paragraph](../../paragraph/).

```cpp
void Aspose::Words::Section::EnsureMinimum()
```


## أمثلة



يوضح كيفية إعداد عقدة قسم جديدة للتحرير.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// يأتي مستند فارغ مع قسم، يحتوي على جسم، والذي بدوره يحتوي على فقرة.
// يمكننا إضافة محتويات إلى هذا المستند عن طريق إضافة عناصر مثل مقاطع النص، الأشكال، أو الجداول إلى تلك الفقرة.
ASSERT_EQ(Aspose::Words::NodeType::Section, doc->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

// إذا أضفنا قسمًا جديدًا بهذه الطريقة، فلن يحتوي على جسم أو أي عقد أطفال أخرى.
doc->get_Sections()->Add(System::MakeObject<Aspose::Words::Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// شغّل طريقة "EnsureMinimum" لإضافة جسم وفقرة إلى هذا القسم لبدء تحريره.
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## انظر أيضًا

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
