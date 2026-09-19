---
title: "Metodo Aspose::Words::CompositeNode::RemoveSmartTags"
linktitle: "RemoveSmartTags"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::CompositeNode::RemoveSmartTags. Rimuove tutti i nodi discendenti SmartTag del nodo corrente in C++."
type: docs
weight: 21000
url: /it/cpp/aspose.words/compositenode/removesmarttags/
---
## CompositeNode::RemoveSmartTags method


Rimuove tutti i nodi discendenti [SmartTag](../../../aspose.words.markup/smarttag/) del nodo corrente.

```cpp
void Aspose::Words::CompositeNode::RemoveSmartTags()
```


## Esempi



Rimuove tutti gli smart tag dai nodi discendenti di un nodo composito.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

ASSERT_EQ(8, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());

doc->RemoveSmartTags();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());
```

## Vedi anche

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
