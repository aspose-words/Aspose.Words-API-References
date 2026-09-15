---
title: "طريقة Aspose::Words::CompositeNode::get_FirstChild"
linktitle: "get_FirstChild"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::CompositeNode::get_FirstChild. يحصل على الطفل الأول للعقدة في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/compositenode/get_firstchild/
---
## CompositeNode::get_FirstChild method


يحصل على الطفل الأول للعقدة.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::get_FirstChild() const
```


## أمثلة



يوضح كيفية استخدام خاصية NextSibling للعقدة لتعداد الأطفال المباشرين لها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

for (System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_FirstChild(); node != nullptr; node = node->get_NextSibling())
{
    std::cout << std::endl;
    std::cout << System::String::Format(u"Node type: {0}", Aspose::Words::Node::NodeTypeToString(node->get_NodeType())) << std::endl;

    System::String contents = node->GetText().Trim();
    std::cout << (contents == System::String::Empty ? u"This node contains no text" : System::String::Format(u"Contents: \"{0}\"", node->GetText().Trim())) << std::endl;
}
```

## انظر أيضًا

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
