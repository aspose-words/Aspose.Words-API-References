---
title: "Aspose::Words::CompositeNode::SelectSingleNode método"
linktitle: "SelectSingleNode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::CompositeNode::SelectSingleNode. Selecciona el primer Node que coincide con la expresión XPath en C++."
type: docs
weight: 23000
url: /es/cpp/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode::SelectSingleNode method


Selecciona el primer [Node](../../node/) que coincide con la expresión XPath.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::SelectSingleNode(const System::String &xpath)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xpath | const System::String\& | La expresión XPath. |

### ReturnValue

El primer [Node](../../node/) que coincide con la consulta XPath o **null** si no se encuentra ningún nodo coincidente.
## Observaciones


Solo se admiten expresiones con nombres de elementos por el momento. No se admiten expresiones que utilicen nombres de atributos.

## Ver también

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
