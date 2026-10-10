---
title: "Aspose::Words::NodeCollection::Add طريقة"
linktitle: "Add"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::NodeCollection::Add طريقة. يضيف عقدة إلى نهاية المجموعة في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/nodecollection/add/
---
## NodeCollection::Add method


يضيف عقدة إلى نهاية المجموعة.

```cpp
void Aspose::Words::NodeCollection::Add(const System::SharedPtr<Aspose::Words::Node> &node)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| node | const System::SharedPtr\<Aspose::Words::Node\>\& | العقدة التي سيتم إضافتها إلى نهاية المجموعة. |
## ملاحظات


يتم إدراج العقدة كطفل داخل كائن العقدة الذي تم إنشاء المجموعة منه.

إذا تم إنشاء العقدة التي يتم إدراجها من مستند آخر، يجب عليك استخدام [ImportNode()](../) لاستيراد العقدة إلى المستند الحالي. يمكن بعد ذلك إدراج العقدة المستوردة في المستند الحالي.

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

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
