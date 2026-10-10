---
title: "Método Aspose::Words::Node::Clone"
linktitle: "Clonar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Node::Clone. Crea un duplicado del nodo en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/node/clone/
---
## Node::Clone method


Crea un duplicado del nodo.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::Clone(bool isCloneChildren)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| isCloneChildren | bool | True para clonar recursivamente el subárbol bajo el nodo especificado; false para clonar solo el nodo en sí. |

### ReturnValue

El nodo clonado.
## Observaciones


Este método sirve como un constructor de copia para nodos. El nodo clonado no tiene padre, pero pertenece al mismo documento que el nodo original.

Este método siempre realiza una copia profunda del nodo. El parámetro *isCloneChildren* especifica si también se debe copiar todos los nodos hijos.

## Ejemplos



Muestra cómo clonar un nodo compuesto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// A continuación se presentan dos formas de clonar un nodo compuesto.
// 1 -  Crear una copia de un nodo y crear también una copia de cada uno de sus nodos hijos.
System::SharedPtr<Aspose::Words::Node> cloneWithChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(true);

ASSERT_TRUE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithChildren))->get_HasChildNodes());
ASSERT_EQ(u"Hello world!", cloneWithChildren->GetText().Trim());

// 2 -  Crear una copia de un nodo solo, sin ningún hijo.
System::SharedPtr<Aspose::Words::Node> cloneWithoutChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(false);

ASSERT_FALSE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithoutChildren))->get_HasChildNodes());
ASSERT_EQ(System::String::Empty, cloneWithoutChildren->GetText().Trim());
```

## Ver también

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
