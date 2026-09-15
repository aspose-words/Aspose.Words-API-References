---
title: "طريقة Aspose::Words::CompositeNode::IndexOf"
linktitle: "IndexOf"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::CompositeNode::IndexOf. تُعيد فهرس العقدة الفرعية المحددة في مصفوفة العقد الفرعية في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words/compositenode/indexof/
---
## CompositeNode::IndexOf method


يعيد فهرس العقدة الفرعية المحددة في مصفوفة العقد الفرعية.

```cpp
int32_t Aspose::Words::CompositeNode::IndexOf(const System::SharedPtr<Aspose::Words::Node> &child)
```


## أمثلة



يوضح كيفية الحصول على فهرس عقدة فرعية معينة من والدها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();

// استرجاع فهرس الفقرة الأخيرة في جسم القسم الأول.
ASSERT_EQ(24, body->GetChildNodes(Aspose::Words::NodeType::Any, false)->IndexOf(body->get_LastParagraph()));
```

## انظر أيضًا

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
