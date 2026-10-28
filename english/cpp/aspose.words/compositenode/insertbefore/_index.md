---
title: Aspose::Words::CompositeNode::InsertBefore method
linktitle: InsertBefore
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CompositeNode::InsertBefore method. Inserts the specified node immediately before the specified reference node in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words/compositenode/insertbefore/
---
## CompositeNode::InsertBefore method


Inserts the specified node immediately before the specified reference node.

```cpp
template<typename T> T Aspose::Words::CompositeNode::InsertBefore(T newChild, const System::SharedPtr<Aspose::Words::Node> & refChild)
```


| Parameter | Type | Description |
| --- | --- | --- |
| newChild | T | The [Node](../../node/) to insert. |
| refChild | const System::SharedPtr\<Aspose::Words::Node\> \& | The [Node](../../node/) that is the reference node. The newChild is placed before this node. |

### ReturnValue

The inserted node.
## Remarks


If refChild is **null**, inserts newChild at the end of the list of child nodes.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use [ImportNode()](../../documentbase/importnode/) to import the node to the current document. The imported node can then be inserted into the current document.
## See Also

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
