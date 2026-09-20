---
title: "Aspose::Words::DocumentBuilder::get_CurrentParagraph método"
linktitle: "get_CurrentParagraph"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::get_CurrentParagraph método. Obtiene el párrafo que está actualmente seleccionado en este DocumentBuilder en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words/documentbuilder/get_currentparagraph/
---
## DocumentBuilder::get_CurrentParagraph method


Obtiene el párrafo que está actualmente seleccionado en este [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::DocumentBuilder::get_CurrentParagraph()
```


## Ejemplos



Muestra cómo mover el cursor de un document builder a diferentes nodos en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Cree un marcador válido, una entidad que consiste en nodos encerrados por un nodo de inicio de marcador,
// y un nodo de fin de marcador.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Bookmark contents.");
builder->EndBookmark(u"MyBookmark");

System::SharedPtr<Aspose::Words::NodeCollection> firstParagraphNodes = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, firstParagraphNodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Run, firstParagraphNodes->idx_get(1)->get_NodeType());
ASSERT_EQ(u"Bookmark contents.", firstParagraphNodes->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::NodeType::BookmarkEnd, firstParagraphNodes->idx_get(2)->get_NodeType());

// El cursor del document builder siempre está delante del nodo que añadimos por última vez con él.
// Si el cursor del builder está al final del documento, su nodo actual será null.
// El nodo anterior es el nodo de fin de marcador que añadimos por última vez.
// Agregar nuevos nodos con el builder los añadirá al último nodo.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// Si deseamos editar una parte diferente del documento con el builder,
// Necesitaremos llevar su cursor al nodo que deseamos editar.
builder->MoveToBookmark(u"MyBookmark");

// Moverlo a un marcador lo moverá al primer nodo dentro de los nodos de inicio y fin del marcador, la ejecución incluida.
ASPOSE_ASSERT_EQ(firstParagraphNodes->idx_get(1), builder->get_CurrentNode());

// También podemos mover el cursor a un nodo individual de esta manera.
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false)->idx_get(0));

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, builder->get_CurrentNode()->get_NodeType());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), builder->get_CurrentParagraph());
ASSERT_TRUE(builder->get_IsAtStartOfParagraph());

// Podemos usar métodos específicos para movernos al inicio/final de un documento.
builder->MoveToDocumentEnd();

ASSERT_TRUE(builder->get_IsAtEndOfParagraph());

builder->MoveToDocumentStart();

ASSERT_TRUE(builder->get_IsAtStartOfParagraph());
```

## Ver también

* Class [Paragraph](../../paragraph/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
