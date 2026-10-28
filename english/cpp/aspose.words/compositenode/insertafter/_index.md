---
title: Aspose::Words::CompositeNode::InsertAfter method
linktitle: InsertAfter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CompositeNode::InsertAfter method. Inserts the specified node immediately after the specified reference node in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words/compositenode/insertafter/
---
## CompositeNode::InsertAfter method


Inserts the specified node immediately after the specified reference node.

```cpp
template<typename T> T Aspose::Words::CompositeNode::InsertAfter(T newChild, const System::SharedPtr<Aspose::Words::Node> & refChild)
```


| Parameter | Type | Description |
| --- | --- | --- |
| newChild | T | The [Node](../../node/) to insert. |
| refChild | const System::SharedPtr\<Aspose::Words::Node\> \& | The [Node](../../node/) that is the reference node. The newChild is placed after the refChild. |

### ReturnValue

The inserted node.
## Remarks


If refChild is **null**, inserts newChild at the beginning of the list of child nodes.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use [ImportNode()](../../documentbase/importnode/) to import the node to the current document. The imported node can then be inserted into the current document.
## See Also

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
