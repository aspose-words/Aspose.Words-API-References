---
title: "Método Aspose::Words::NodeCollection::Add"
linktitle: "Add"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::NodeCollection::Add. Añade un nodo al final de la colección en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/nodecollection/add/
---
## NodeCollection::Add method


Agrega un nodo al final de la colección.

```cpp
void Aspose::Words::NodeCollection::Add(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nodo | const System::SharedPtr\<Aspose::Words::Node\>\& | El nodo que se añadirá al final de la colección. |
## Observaciones


El nodo se inserta como hijo en el objeto nodo del cual se creó la colección.

Si el nodo que se está insertando fue creado a partir de otro documento, debe usar [ImportNode()](../) para importar el nodo al documento actual. El nodo importado puede entonces insertarse en el documento actual.

## Ejemplos



Muestra cómo preparar un nuevo nodo de sección para editar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento en blanco viene con una sección, que tiene un cuerpo, que a su vez tiene un párrafo.
// Podemos agregar contenido a este documento añadiendo elementos como ejecuciones de texto, formas o tablas a ese párrafo.
ASSERT_EQ(Aspose::Words::NodeType::Section, doc->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

// Si añadimos una nueva sección de esta manera, no tendrá un cuerpo ni ningún otro nodo hijo.
doc->get_Sections()->Add(System::MakeObject<Aspose::Words::Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Ejecute el método \"EnsureMinimum\" para agregar un cuerpo y un párrafo a esta sección y comenzar a editarla.
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Ver también

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
