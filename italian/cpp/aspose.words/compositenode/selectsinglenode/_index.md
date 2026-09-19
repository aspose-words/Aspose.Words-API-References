---
title: "Metodo Aspose::Words::CompositeNode::SelectSingleNode"
linktitle: "SelectSingleNode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::CompositeNode::SelectSingleNode. Seleziona il primo Node che corrisponde all'espressione XPath in C++."
type: docs
weight: 23000
url: /it/cpp/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode::SelectSingleNode method


Seleziona il primo [Node](../../node/) che corrisponde all'espressione XPath.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::SelectSingleNode(const System::String &xpath)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xpath | const System::String\& | L'espressione XPath. |

### ReturnValue

Il primo [Node](../../node/) che corrisponde alla query XPath o **null** se non viene trovato alcun nodo corrispondente.
## Note


Al momento sono supportate solo le espressioni con nomi di elemento. Le espressioni che utilizzano nomi di attributo non sono supportate.

## Vedi anche

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
