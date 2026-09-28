---
title: "Метод Aspose::Words::Node::get_NextSibling"
linktitle: "get_NextSibling"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Node::get_NextSibling. Получает узел, непосредственно следующий за этим узлом в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words/node/get_nextsibling/
---
## Node::get_NextSibling method


Возвращает узел, непосредственно следующий за этим узлом.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_NextSibling()
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

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
