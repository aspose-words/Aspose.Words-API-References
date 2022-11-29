---
title: Remove
second_title: Aspose.Words for C++ API Reference
description: Removes itself from the parent.
type: docs
weight: 196
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
auto doc = MakeObject<Document>(MyDir + u"Images.docx");
SharedPtr<NodeCollection> shapes = doc->GetChildNodes(NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_OfType<SharedPtr<Shape>>()->LINQ_Count([](SharedPtr<Shape> s) { return s->get_HasImage(); }));

for (const auto& shape : System::IterateOver(shapes->LINQ_OfType<SharedPtr<Shape>>()))
{
    if (shape->get_HasImage())
    {
        shape->Remove();
    }
}

ASSERT_EQ(0, shapes->LINQ_OfType<SharedPtr<Shape>>()->LINQ_Count([](SharedPtr<Shape> s) { return s->get_HasImage(); }));
```


Shows how to remove all child nodes of a specific type from a composite node. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Tables.docx");

ASSERT_EQ(2, doc->GetChildNodes(NodeType::Table, true)->get_Count());

SharedPtr<Node> curNode = doc->get_FirstSection()->get_Body()->get_FirstChild();

while (curNode != nullptr)
{
    // Save the next sibling node as a variable in case we want to move to it after deleting this node.
    SharedPtr<Node> nextNode = curNode->get_NextSibling();

    // A section body can contain Paragraph and Table nodes.
    // If the node is a Table, remove it from the parent.
    if (curNode->get_NodeType() == NodeType::Table)
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0, doc->GetChildNodes(NodeType::Table, true)->get_Count());
```

## See Also

* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
