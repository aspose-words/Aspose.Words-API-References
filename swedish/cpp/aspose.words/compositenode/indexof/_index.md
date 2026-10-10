---
title: "Aspose::Words::CompositeNode::IndexOf metod"
linktitle: "IndexOf"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::CompositeNode::IndexOf metod. Returnerar indexet för den angivna undernoden i undernodsarrayen i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words/compositenode/indexof/
---
## CompositeNode::IndexOf method


Returnerar indexet för den angivna barnnoden i barnnodarrayen.

```cpp
int32_t Aspose::Words::CompositeNode::IndexOf(const System::SharedPtr<Aspose::Words::Node> &child)
```


## Exempel



Visar hur man får indexet för en given undernod från dess förälder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();

// Hämta indexet för det sista stycket i kroppen av den första sektionen.
ASSERT_EQ(24, body->GetChildNodes(Aspose::Words::NodeType::Any, false)->IndexOf(body->get_LastParagraph()));
```

## Se även

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
