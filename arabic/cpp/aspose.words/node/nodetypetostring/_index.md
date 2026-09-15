---
title: "طريقة Aspose::Words::Node::NodeTypeToString"
linktitle: "NodeTypeToString"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Node::NodeTypeToString. طريقة مساعدة تقوم بتحويل قيمة تعداد نوع العقدة إلى سلسلة صديقة للمستخدم في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words/node/nodetypetostring/
---
## Node::NodeTypeToString method


طريقة مساعدة تقوم بتحويل قيمة تعداد نوع العقدة إلى سلسلة صديقة للمستخدم.

```cpp
static System::String Aspose::Words::Node::NodeTypeToString(Aspose::Words::NodeType nodeType)
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

* Enum [NodeType](../../nodetype/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
