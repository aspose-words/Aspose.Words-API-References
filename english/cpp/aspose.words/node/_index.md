---
title: Node
second_title: Aspose.Words for C++ API Reference
description: Base class for all nodes of a Word document.
type: docs
weight: 521
url: /cpp/aspose.words/node/
---
## Node class


Base class for all nodes of a Word document.

```cpp
class Node : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepts a visitor. |
| [Clone](./clone/)(bool) | Creates a duplicate of the node. |
| [get_CustomNodeId](./get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](./get_document/)() const | Gets the document to which this node belongs. |
| virtual [get_IsComposite](./get_iscomposite/)() | Returns true if this node can contain other nodes. |
| [get_NextSibling](./get_nextsibling/)() | Gets the node immediately following this node. |
| virtual [get_NodeType](./get_nodetype/)() const | Gets the type of this node. |
| [get_ParentNode](./get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PreviousSibling](./get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](./get_range/)() | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [GetAncestor](./getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
| [GetAncestorOf](./getancestorof/)() |  |
| virtual [GetText](./gettext/)() | Gets the text of this node and of all its children. |
| [NextPreOrder](./nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](./nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](./previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](./remove/)() | Removes itself from the parent. |
| [set_CustomNodeId](./set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](./get_customnodeid/). |
| [ToString](./tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](./tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |

A document is represented as a tree of nodes, similar to DOM or XmlDocument.

For more info see the Composite design pattern.

The [Node](./) class:

* Defines the child node interface.
* Defines the interface for visiting nodes.
* Provides default cloning capability.
* Implements parent node and owner document mechanisms.
* Implements access to sibling nodes.



## Examples




Shows how to clone a composite node. 
```cpp
auto doc = MakeObject<Document>();
SharedPtr<Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
para->AppendChild(MakeObject<Run>(doc, u"Hello world!"));

// Below are two ways of cloning a composite node.
// 1 -  Create a clone of a node, and create a clone of each of its child nodes as well.
SharedPtr<Node> cloneWithChildren = para->Clone(true);

ASSERT_TRUE((System::DynamicCast<CompositeNode>(cloneWithChildren))->get_HasChildNodes());
ASSERT_EQ(u"Hello world!", cloneWithChildren->GetText().Trim());

// 2 -  Create a clone of a node just by itself without any children.
SharedPtr<Node> cloneWithoutChildren = para->Clone(false);

ASSERT_FALSE((System::DynamicCast<CompositeNode>(cloneWithoutChildren))->get_HasChildNodes());
ASSERT_EQ(String::Empty, cloneWithoutChildren->GetText().Trim());
```


Shows how to traverse through a composite node's collection of child nodes. 
```cpp
auto doc = MakeObject<Document>();

// Add two runs and one shape as child nodes to the first paragraph of this document.
auto paragraph = System::DynamicCast<Paragraph>(doc->GetChild(NodeType::Paragraph, 0, true));
paragraph->AppendChild(MakeObject<Run>(doc, u"Hello world! "));

auto shape = MakeObject<Shape>(doc, ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
shape->set_CustomNodeId(100);
shape->set_WrapType(WrapType::Inline);
paragraph->AppendChild(shape);

paragraph->AppendChild(MakeObject<Run>(doc, u"Hello again!"));

// Iterate through the paragraph's collection of immediate children,
// and print any runs or shapes that we find within.
SharedPtr<NodeCollection> children = paragraph->get_ChildNodes();

ASSERT_EQ(3, paragraph->get_ChildNodes()->get_Count());

for (const auto& child : System::IterateOver(children))
{
    switch (child->get_NodeType())
    {
    case NodeType::Run:
        std::cout << "Run contents:" << std::endl;
        std::cout << "\t\"" << child->GetText().Trim() << "\"" << std::endl;
        break;

    case NodeType::Shape: {
        auto childShape = System::DynamicCast<Shape>(child);
        std::cout << "Shape:" << std::endl;
        std::cout << String::Format(u"\t{0}, {1}x{2}", childShape->get_ShapeType(), childShape->get_Width(), childShape->get_Height()) << std::endl;
        ASSERT_EQ(100, shape->get_CustomNodeId());
        break;
    }

    default:
        break;
    }
}
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

