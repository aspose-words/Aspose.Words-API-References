---
title: "Aspose::Words::CompositeNode::SelectSingleNode Methode"
linktitle: "SelectSingleNode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::CompositeNode::SelectSingleNode Methode. Wählt den ersten Node aus, der dem XPath-Ausdruck in C++ entspricht."
type: docs
weight: 23000
url: /de/cpp/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode::SelectSingleNode method


Wählt den ersten [Node](../../node/) aus, der dem XPath-Ausdruck entspricht.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::SelectSingleNode(const System::String &xpath)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xpath | const System::String\& | Der XPath-Ausdruck. |

### ReturnValue

Der erste [Node](../../node/) der der XPath-Abfrage entspricht oder **null**, wenn kein passender Knoten gefunden wird.
## Hinweise


Derzeit werden nur Ausdrücke mit Elementnamen unterstützt. Ausdrücke, die Attributnamen verwenden, werden nicht unterstützt.

## Siehe auch

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
