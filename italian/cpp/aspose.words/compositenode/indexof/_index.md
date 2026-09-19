---
title: "Metodo Aspose::Words::CompositeNode::IndexOf"
linktitle: "IndexOf"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::CompositeNode::IndexOf. Restituisce l'indice del nodo figlio specificato nell'array dei nodi figlio in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words/compositenode/indexof/
---
## CompositeNode::IndexOf method


Restituisce l'indice del nodo figlio specificato nell'array dei nodi figlio.

```cpp
int32_t Aspose::Words::CompositeNode::IndexOf(const System::SharedPtr<Aspose::Words::Node> &child)
```


## Esempi



Mostra come ottenere l'indice di un nodo figlio dato dal suo genitore.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();

// Recupera l'indice dell'ultimo paragrafo nel corpo della prima sezione.
ASSERT_EQ(24, body->GetChildNodes(Aspose::Words::NodeType::Any, false)->IndexOf(body->get_LastParagraph()));
```

## Vedi anche

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
