---
title: "Aspose::Words::Node::NodeTypeToString метод"
linktitle: "NodeTypeToString"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Node::NodeTypeToString метод. Утилитный метод, который преобразует значение перечисления типа узла в удобочитаемую строку в C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words/node/nodetypetostring/
---
## Node::NodeTypeToString method


Вспомогательный метод, преобразующий значение перечисления типа узла в удобочитаемую строку.

```cpp
static System::String Aspose::Words::Node::NodeTypeToString(Aspose::Words::NodeType nodeType)
```


## Примеры



Показывает, как использовать свойство NextSibling узла для перечисления его непосредственных дочерних элементов.
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

## См. также

* Enum [NodeType](../../nodetype/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
