---
title: PreviousPreOrder
second_title: Aspose.Words for C++ API Reference
description: Gets the previous node according to the pre-order tree traversal algorithm.
type: docs
weight: 183
url: /cpp/aspose.words/node/previouspreorder/
---
## Node.PreviousPreOrder method


Gets the previous node according to the pre-order tree traversal algorithm.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::PreviousPreOrder(const System::SharedPtr<Aspose::Words::Node> &rootNode)
```


| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | const System::SharedPtr\<Aspose::Words::Node\>\& | The top node (limit) of traversal. |

### ReturnValue


Previous node in pre-order order. Null if reached the rootNode.

## Examples




Shows how to traverse the document's node tree using the pre-order traversal algorithm, and delete any encountered shape with an image. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Images.docx");

ASSERT_EQ(9,
          doc->GetChildNodes(NodeType::Shape, true)->LINQ_OfType<SharedPtr<Shape>>()->LINQ_Count([](SharedPtr<Shape> s) { return s->get_HasImage(); }));

SharedPtr<Node> curNode = doc;
while (curNode != nullptr)
{
    SharedPtr<Node> nextNode = curNode->NextPreOrder(doc);

    if (curNode->PreviousPreOrder(doc) != nullptr && nextNode != nullptr)
    {
        ASPOSE_ASSERT_EQ(curNode, nextNode->PreviousPreOrder(doc));
    }

    if (curNode->get_NodeType() == NodeType::Shape && (System::DynamicCast<Shape>(curNode))->get_HasImage())
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0,
          doc->GetChildNodes(NodeType::Shape, true)->LINQ_OfType<SharedPtr<Shape>>()->LINQ_Count([](SharedPtr<Shape> s) { return s->get_HasImage(); }));
```

