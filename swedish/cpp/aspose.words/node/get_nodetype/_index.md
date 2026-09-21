---
title: "Aspose::Words::Node::get_NodeType metod"
linktitle: "get_NodeType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Node::get_NodeType metod. Hämtar typen av denna nod i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words/node/get_nodetype/
---
## Node::get_NodeType method


Hämtar typen av denna nod.

```cpp
virtual Aspose::Words::NodeType Aspose::Words::Node::get_NodeType() const =0
```


## Exempel



Visar hur man tar bort alla barnnoder av en specifik typ från en sammansatt nod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());

System::SharedPtr<Aspose::Words::Node> curNode = doc->get_FirstSection()->get_Body()->get_FirstChild();

while (curNode != nullptr)
{
    // Spara nästa syskonnod som en variabel ifall vi vill flytta till den efter att ha raderat denna nod.
    System::SharedPtr<Aspose::Words::Node> nextNode = curNode->get_NextSibling();

    // En sektionskropp kan innehålla Paragraph- och Table-noder.
    // Om noden är en Table, ta bort den från föräldern.
    if (curNode->get_NodeType() == Aspose::Words::NodeType::Table)
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());
```


Visar hur man använder en nods NextSibling‑egenskap för att iterera genom dess omedelbara barn.
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

## Se även

* Enum [NodeType](../../nodetype/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
