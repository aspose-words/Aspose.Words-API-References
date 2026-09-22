---
title: "Aspose::Words::Node::NodeTypeToString yöntemi"
linktitle: "NodeTypeToString"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Node::NodeTypeToString yöntemi. C++'ta bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem."
type: docs
weight: 1000
url: /tr/cpp/aspose.words/node/nodetypetostring/
---
## Node::NodeTypeToString method


Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem.

```cpp
static System::String Aspose::Words::Node::NodeTypeToString(Aspose::Words::NodeType nodeType)
```


## Örnekler



Bir düğümün NextSibling özelliğini kullanarak doğrudan çocuklarını nasıl yineleyeceğinizi gösterir.
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

## Ayrıca Bakınız

* Enum [NodeType](../../nodetype/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
