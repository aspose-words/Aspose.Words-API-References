---
title: Aspose::Words::CompositeNode::AppendChild method
linktitle: AppendChild
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CompositeNode::AppendChild method. Adds the specified node to the end of the list of child nodes for this node in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/compositenode/appendchild/
---
## CompositeNode::AppendChild method


Adds the specified node to the end of the list of child nodes for this node.

```cpp
template<typename T> T Aspose::Words::CompositeNode::AppendChild(T newChild)
```


| Parameter | Type | Description |
| --- | --- | --- |
| newChild | T | The node to add. |

### ReturnValue

The node added.
## Remarks


If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use [ImportNode()](../../documentbase/importnode/) to import the node to the current document. The imported node can then be inserted into the current document.
## See Also

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
