---
title: "Aspose::Words::Node::get_NextSibling yöntemi"
linktitle: "get_NextSibling"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Node::get_NextSibling yöntemi. Bu düğümden hemen sonra gelen düğümü C++'da alır."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/node/get_nextsibling/
---
## Node::get_NextSibling method


Bu düğümü hemen izleyen düğümü alır.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_NextSibling()
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

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
