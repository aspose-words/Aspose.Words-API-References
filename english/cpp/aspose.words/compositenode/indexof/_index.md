---
title: IndexOf
second_title: Aspose.Words for C++ API Reference
description: Returns the index of the specified child node in the child node array.
type: docs
weight: 144
url: /cpp/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method


Returns the index of the specified child node in the child node array.

```cpp
int32_t Aspose::Words::CompositeNode::IndexOf(const System::SharedPtr<Aspose::Words::Node> &child)
```


## Examples




Shows how to get the index of a given child node from its parent. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

SharedPtr<Body> body = doc->get_FirstSection()->get_Body();

// Retrieve the index of the last paragraph in the body of the first section.
ASSERT_EQ(24, body->get_ChildNodes()->IndexOf(body->get_LastParagraph()));
```

