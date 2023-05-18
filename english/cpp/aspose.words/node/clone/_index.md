---
title: Aspose::Words::Node::Clone method
linktitle: Clone
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Node::Clone method. Creates a duplicate of the node in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/node/clone/
---
## Node::Clone method


Creates a duplicate of the node.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::Clone(bool isCloneChildren)
```


| Parameter | Type | Description |
| --- | --- | --- |
| isCloneChildren | bool | True to recursively clone the subtree under the specified node; false to clone only the node itself. |

### ReturnValue

The cloned node.
## Remarks


This method serves as a copy constructor for nodes. The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The *isCloneChildren* parameter specifies whether to perform copy all child nodes as well.

## Examples



Shows how to clone a composite node. 
```cpp
auto doc = MakeObject<Document>();
SharedPtr<Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
para->AppendChild(MakeObject<Run>(doc, u"Hello world!"));

// Below are two ways of cloning a composite node.
// 1 -  Create a clone of a node, and create a clone of each of its child nodes as well.
SharedPtr<Node> cloneWithChildren = para->Clone(true);

ASSERT_TRUE((System::ExplicitCast<CompositeNode>(cloneWithChildren))->get_HasChildNodes());
ASSERT_EQ(u"Hello world!", cloneWithChildren->GetText().Trim());

// 2 -  Create a clone of a node just by itself without any children.
SharedPtr<Node> cloneWithoutChildren = para->Clone(false);

ASSERT_FALSE((System::ExplicitCast<CompositeNode>(cloneWithoutChildren))->get_HasChildNodes());
ASSERT_EQ(String::Empty, cloneWithoutChildren->GetText().Trim());
```

## See Also

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
