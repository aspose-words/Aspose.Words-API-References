---
title: "Aspose::Words::CompositeNode::IndexOf Methode"
linktitle: "IndexOf"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::CompositeNode::IndexOf Methode. Gibt den Index des angegebenen untergeordneten Knotens im Array der untergeordneten Knoten in C++ zurück."
type: docs
weight: 14000
url: /de/cpp/aspose.words/compositenode/indexof/
---
## CompositeNode::IndexOf method


Gibt den Index des angegebenen Kindknotens im Kindknoten-Array zurück.

```cpp
int32_t Aspose::Words::CompositeNode::IndexOf(const System::SharedPtr<Aspose::Words::Node> &child)
```


## Beispiele



Zeigt, wie man den Index eines bestimmten untergeordneten Knotens von seinem übergeordneten Knoten erhält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();

// Rufe den Index des letzten Absatzes im Body des ersten Abschnitts ab.
ASSERT_EQ(24, body->GetChildNodes(Aspose::Words::NodeType::Any, false)->IndexOf(body->get_LastParagraph()));
```

## Siehe auch

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
