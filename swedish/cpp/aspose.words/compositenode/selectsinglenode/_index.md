---
title: "Aspose::Words::CompositeNode::SelectSingleNode metod"
linktitle: "SelectSingleNode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::CompositeNode::SelectSingleNode metod. Väljer den första Node som matchar XPath-uttrycket i C++."
type: docs
weight: 23000
url: /sv/cpp/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode::SelectSingleNode method


Väljer den första [Node](../../node/) som matchar XPath-uttrycket.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::SelectSingleNode(const System::String &xpath)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| xpath | const System::String\& | XPath-uttrycket. |

### ReturnValue

Den första [Node](../../node/) som matchar XPath-frågan eller **null** om ingen matchande nod hittas.
## Anmärkningar


Endast uttryck med elementnamn stöds för närvarande. Uttryck som använder attributnamn stöds inte.

## Se även

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
