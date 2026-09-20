---
title: "Método Aspose::Words::CompositeNode::IndexOf"
linktitle: "IndexOf"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::CompositeNode::IndexOf method. Devuelve el índice del nodo hijo especificado en la matriz de nodos hijos en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words/compositenode/indexof/
---
## CompositeNode::IndexOf method


Devuelve el índice del nodo hijo especificado en la matriz de nodos hijos.

```cpp
int32_t Aspose::Words::CompositeNode::IndexOf(const System::SharedPtr<Aspose::Words::Node> &child)
```


## Ejemplos



Muestra cómo obtener el índice de un nodo hijo dado a partir de su padre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();

// Recupera el índice del último párrafo en el cuerpo de la primera sección.
ASSERT_EQ(24, body->GetChildNodes(Aspose::Words::NodeType::Any, false)->IndexOf(body->get_LastParagraph()));
```

## Ver también

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
