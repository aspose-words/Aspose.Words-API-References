---
title: "Aspose::Words::Node::get_NodeType метод"
linktitle: "get_NodeType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Node::get_NodeType метод. Получает тип этого узла в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words/node/get_nodetype/
---
## Node::get_NodeType method


Возвращает тип этого узла.

```cpp
virtual Aspose::Words::NodeType Aspose::Words::Node::get_NodeType() const =0
```


## Примеры



Показывает, как удалить все дочерние узлы определённого типа из составного узла.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());

System::SharedPtr<Aspose::Words::Node> curNode = doc->get_FirstSection()->get_Body()->get_FirstChild();

while (curNode != nullptr)
{
    // Сохраните следующий соседний узел в переменную на случай, если нам понадобится перейти к нему после удаления текущего узла.
    System::SharedPtr<Aspose::Words::Node> nextNode = curNode->get_NextSibling();

    // Тело раздела может содержать узлы Paragraph и Table.
    // Если узел является таблицей, удалите его из родителя.
    if (curNode->get_NodeType() == Aspose::Words::NodeType::Table)
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());
```


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
