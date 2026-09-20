---
title: "Método Aspose::Words::Node::get_ParentNode"
linktitle: "get_ParentNode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Node::get_ParentNode. Obtiene el padre inmediato de este nodo en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words/node/get_parentnode/
---
## Node::get_ParentNode method


Obtiene el padre inmediato de este nodo.

```cpp
System::SharedPtr<Aspose::Words::CompositeNode> Aspose::Words::Node::get_ParentNode()
```

## Observaciones


Si un nodo acaba de ser creado y aún no se ha añadido al árbol, o si ha sido eliminado del árbol, el padre es **null**.

## Ejemplos



Muestra cómo acceder al nodo padre de un nodo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Añade un nodo Run hijo al primer párrafo del documento.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// El párrafo es el nodo padre del nodo run. Podemos rastrear esta línea de descendencia
// hasta el nodo documento, que es la raíz del árbol de nodos del documento.
ASPOSE_ASSERT_EQ(para, run->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection(), doc->get_FirstSection()->get_Body()->get_ParentNode());
ASPOSE_ASSERT_EQ(doc, doc->get_FirstSection()->get_ParentNode());
```


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

* Class [CompositeNode](../../compositenode/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
