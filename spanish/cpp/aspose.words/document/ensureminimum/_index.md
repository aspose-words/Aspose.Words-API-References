---
title: "Método Aspose::Words::Document::EnsureMinimum"
linktitle: "EnsureMinimum"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::EnsureMinimum. Si el documento no contiene secciones, crea una sección con un párrafo en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words/document/ensureminimum/
---
## Document::EnsureMinimum method


Si el documento no contiene secciones, crea una sección con un párrafo.

```cpp
void Aspose::Words::Document::EnsureMinimum()
```


## Ejemplos



Muestra cómo asegurar que un documento contenga el conjunto mínimo de nodos necesario para editar su contenido.
```cpp
// Un documento recién creado contiene una sección hija, que incluye un cuerpo hijo y un párrafo hijo.
// Podemos editar el contenido del cuerpo del documento añadiendo nodos como Runs o Shapes en línea a ese párrafo.
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASPOSE_ASSERT_EQ(doc, nodes->idx_get(0)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(0), nodes->idx_get(1)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(1), nodes->idx_get(2)->get_ParentNode());

// Este es el conjunto mínimo de nodos que necesitamos para poder editar el documento.
// Ya no podremos editar el documento si eliminamos alguno de ellos.
doc->RemoveAllChildren();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Llame a este método para asegurarse de que el documento tenga al menos esos tres nodos, de modo que podamos volver a editarlo.
doc->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());

(System::ExplicitCast<Aspose::Words::Paragraph>(nodes->idx_get(2)))->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
