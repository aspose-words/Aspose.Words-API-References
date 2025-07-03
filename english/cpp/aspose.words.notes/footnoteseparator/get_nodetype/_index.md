---
title: Aspose::Words::Notes::FootnoteSeparator::get_NodeType method
linktitle: get_NodeType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Notes::FootnoteSeparator::get_NodeType method. Gets the type of this node in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.notes/footnoteseparator/get_nodetype/
---
## FootnoteSeparator::get_NodeType method


Gets the type of this node.

```cpp
Aspose::Words::NodeType Aspose::Words::Notes::FootnoteSeparator::get_NodeType() const override
```


## Examples



Shows how to remove all child nodes of a specific type from a composite node. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());

System::SharedPtr<Aspose::Words::Node> curNode = doc->get_FirstSection()->get_Body()->get_FirstChild();

while (curNode != nullptr)
{
    // Save the next sibling node as a variable in case we want to move to it after deleting this node.
    System::SharedPtr<Aspose::Words::Node> nextNode = curNode->get_NextSibling();

    // A section body can contain Paragraph and Table nodes.
    // If the node is a Table, remove it from the parent.
    if (curNode->get_NodeType() == Aspose::Words::NodeType::Table)
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());
```


Shows how to use a node's NextSibling property to enumerate through its immediate children. 
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

## See Also

* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [FootnoteSeparator](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
