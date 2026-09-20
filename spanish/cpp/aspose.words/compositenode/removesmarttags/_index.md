---
title: "Aspose::Words::CompositeNode::RemoveSmartTags método"
linktitle: "RemoveSmartTags"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::CompositeNode::RemoveSmartTags método. Elimina todos los nodos descendientes SmartTag del nodo actual en C++."
type: docs
weight: 21000
url: /es/cpp/aspose.words/compositenode/removesmarttags/
---
## CompositeNode::RemoveSmartTags method


Elimina todos los nodos descendientes de [SmartTag](../../../aspose.words.markup/smarttag/) del nodo actual.

```cpp
void Aspose::Words::CompositeNode::RemoveSmartTags()
```


## Ejemplos



Elimina todas las etiquetas inteligentes de los nodos descendientes de un nodo compuesto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

ASSERT_EQ(8, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());

doc->RemoveSmartTags();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());
```

## Ver también

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
