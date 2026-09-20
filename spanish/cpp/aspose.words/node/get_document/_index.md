---
title: "Método Aspose::Words::Node::get_Document"
linktitle: "get_Document"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Node::get_Document. Obtiene el documento al que pertenece este nodo en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/node/get_document/
---
## Node::get_Document method


Obtiene el documento al que pertenece este nodo.

```cpp
virtual System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::Node::get_Document() const
```

## Observaciones


El nodo siempre pertenece a un documento, incluso si acaba de ser creado y aún no se ha añadido al árbol, o si ha sido removido del árbol.

## Ejemplos



Muestra cómo crear un nodo y establecer su documento propietario.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Aún no hemos añadido este párrafo como hijo a ningún nodo compuesto.
ASSERT_TRUE(System::TestTools::IsNull(para->get_ParentNode()));

// Si un nodo es un tipo de nodo hijo apropiado de otro nodo compuesto,
// podemos adjuntarlo como hijo solo si ambos nodos tienen el mismo documento propietario.
// El documento propietario es el documento que pasamos al constructor del nodo.
// No hemos adjuntado este párrafo al documento, por lo que el documento no contiene su texto.
ASPOSE_ASSERT_EQ(para->get_Document(), doc);
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());

// Dado que el documento posee este párrafo, podemos aplicar uno de sus estilos al contenido del párrafo.
para->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));

// Agregue este nodo al documento y luego verifique su contenido.
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Ver también

* Class [DocumentBase](../../documentbase/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
