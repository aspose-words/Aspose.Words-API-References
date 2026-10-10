---
title: "طريقة Aspose::Words::Document::EnsureMinimum"
linktitle: "EnsureMinimum"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::EnsureMinimum. إذا كان المستند لا يحتوي على أقسام، فإنها تنشئ قسمًا واحدًا مع فقرة واحدة في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words/document/ensureminimum/
---
## Document::EnsureMinimum method


إذا لم يحتوي المستند على أقسام، ينشئ قسمًا واحدًا مع فقرة واحدة.

```cpp
void Aspose::Words::Document::EnsureMinimum()
```


## أمثلة



يوضح كيفية التأكد من أن المستند يحتوي على الحد الأدنى من العقد المطلوبة لتحرير محتوياته.
```cpp
// المستند الذي تم إنشاؤه حديثًا يحتوي على قسم فرعي واحد، والذي يتضمن جسمًا فرعيًا واحدًا وفقرة فرعية واحدة.
// يمكننا تحرير محتويات جسم المستند بإضافة عقد مثل Runs أو Shapes داخلية إلى تلك الفقرة.
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASPOSE_ASSERT_EQ(doc, nodes->idx_get(0)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(0), nodes->idx_get(1)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(1), nodes->idx_get(2)->get_ParentNode());

// هذه هي مجموعة العقد الحد الأدنى التي نحتاجها لتتمكن من تحرير المستند.
// لن نتمكن بعد الآن من تحرير المستند إذا حذفنا أيًا منها.
doc->RemoveAllChildren();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// استدعِ هذه الطريقة للتأكد من أن المستند يحتوي على الأقل على تلك العقد الثلاثة حتى نتمكن من تحريره مرة أخرى.
doc->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());

(System::ExplicitCast<Aspose::Words::Paragraph>(nodes->idx_get(2)))->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
