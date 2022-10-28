---
title: SelectSingleNode
second_title: Aspose.Words for C++ API Reference
description: Selects the first Node that matches the XPath expression.
type: docs
weight: 248
url: /cpp/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method


Selects the first [Node](../../node/) that matches the XPath expression.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::SelectSingleNode(const System::String &xpath)
```


| Parameter | Type | Description |
| --- | --- | --- |
| xpath | const System::String\& | The XPath expression. |

### ReturnValue


The first [Node](../../node/) that matches the XPath query or null if no matching node is found.

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.


