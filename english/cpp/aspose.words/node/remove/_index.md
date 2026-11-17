---
title: Aspose::Words::Node::Remove method
linktitle: Remove
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Node::Remove method. Removes itself from the parent in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words/node/remove/
---
## Node::Remove method


Removes itself from the parent.

```cpp
void Aspose::Words::Node::Remove()
```

## Examples


Shows how to delete all shapes with images from a document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Images.docx"));
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(NodeType::Shape, true);

ASSERT_EQ(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape>>()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_HasImage();
}))), 9);

for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape>>()))
{
    if (shape->get_HasImage())
    {
        shape->Remove();
    }
}

ASSERT_EQ(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape>>()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_HasImage();
}))), 0);
```

Shows how to remove all child nodes of a specific type from a composite node.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Tables.docx"));

ASSERT_EQ(doc->GetChildNodes(NodeType::Table, true)->get_Count(), 2);

System::SharedPtr<Aspose::Words::Node> curNode = doc->get_FirstSection()->get_Body()->get_FirstChild();

while (curNode != nullptr)
{
    // Save the next sibling node as a variable in case we want to move to it after deleting this node.
    System::SharedPtr<Aspose::Words::Node> nextNode = curNode->get_NextSibling();

    // A section body can contain Paragraph and Table nodes.
    // If the node is a Table, remove it from the parent.
    if (curNode->get_NodeType() == NodeType::Table)
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(doc->GetChildNodes(NodeType::Table, true)->get_Count(), 0);
```
## See Also

* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
