---
title: Aspose::Words::CompositeNode::IndexOf method
linktitle: IndexOf
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CompositeNode::IndexOf method. Returns the index of the specified child node in the child node array in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words/compositenode/indexof/
---
## CompositeNode::IndexOf method


Returns the index of the specified child node in the child node array.

```cpp
int32_t Aspose::Words::CompositeNode::IndexOf(const System::SharedPtr<Aspose::Words::Node> &child)
```


## Examples



Shows how to get the index of a given child node from its parent. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();

// Retrieve the index of the last paragraph in the body of the first section.
ASSERT_EQ(24, body->GetChildNodes(Aspose::Words::NodeType::Any, false)->IndexOf(body->get_LastParagraph()));
```

## See Also

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
