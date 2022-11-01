---
title: get_NodeType
second_title: Aspose.Words for C++ API Reference
description: Gets the type of this node.
type: docs
weight: 144
url: /cpp/aspose.words.markup/structureddocumenttagrangestart/get_nodetype/
---
## StructuredDocumentTagRangeStart.get_NodeType method


Gets the type of this node.

```cpp
Aspose::Words::NodeType Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_NodeType() const override
```


## Examples




Shows how to traverse a composite node's tree of child nodes. 
```cpp
void RecurseChildren()
{
    auto doc = MakeObject<Document>(MyDir + u"Paragraphs.docx");

    // Any node that can contain child nodes, such as the document itself, is composite.
    ASSERT_TRUE(doc->get_IsComposite());

    // Invoke the recursive function that will go through and print all the child nodes of a composite node.
    TraverseAllNodes(doc, 0);
}

void TraverseAllNodes(SharedPtr<CompositeNode> parentNode, int depth)
{
    for (SharedPtr<Node> childNode = parentNode->get_FirstChild(); childNode != nullptr; childNode = childNode->get_NextSibling())
    {
        std::cout << (String(u'\t', depth)) << Node::NodeTypeToString(childNode->get_NodeType());

        // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
        if (childNode->get_IsComposite())
        {
            std::cout << std::endl;
            TraverseAllNodes(System::DynamicCast<CompositeNode>(childNode), depth + 1);
        }
        else if (System::ObjectExt::Is<Inline>(childNode))
        {
            std::cout << " - \"" << childNode->GetText().Trim() << "\"" << std::endl;
        }
        else
        {
            std::cout << std::endl;
        }
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


Shows how to use a node's NextSibling property to enumerate through its immediate children. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Paragraphs.docx");

for (SharedPtr<Node> node = doc->get_FirstSection()->get_Body()->get_FirstChild(); node != nullptr; node = node->get_NextSibling())
{
    std::cout << std::endl;
    std::cout << "Node type: " << Node::NodeTypeToString(node->get_NodeType()) << std::endl;

    String contents = node->GetText().Trim();
    std::cout << (contents == String::Empty ? u"This node contains no text" : String::Format(u"Contents: \"{0}\"", node->GetText().Trim()))
              << std::endl;
}
```

