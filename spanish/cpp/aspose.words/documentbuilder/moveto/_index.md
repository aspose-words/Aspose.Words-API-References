---
title: "Método Aspose::Words::DocumentBuilder::MoveTo"
linktitle: "MoveTo"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBuilder::MoveTo. Mueve el cursor a un nodo en línea o al final de un párrafo en C++."
type: docs
weight: 51000
url: /es/cpp/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder::MoveTo method


Mueve el cursor a un nodo en línea o al final de un párrafo.

```cpp
void Aspose::Words::DocumentBuilder::MoveTo(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nodo | const System::SharedPtr\<Aspose::Words::Node\>\& | El nodo debe ser un párrafo o un hijo directo de un párrafo. |
## Observaciones


Cuando *node* es un nodo a nivel en línea, el cursor se mueve a este nodo y el contenido adicional se insertará antes de ese nodo.

Cuando *node* es un [Paragraph](../../paragraph/), el cursor se mueve al final del párrafo y el contenido adicional se insertará justo antes del salto de párrafo.

Cuando *node* es un nodo a nivel de bloque pero no un [Paragraph](../../paragraph/), el cursor se mueve al final del primer párrafo dentro del nodo de bloque y el contenido adicional se insertará justo antes del salto de párrafo.

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


Muestra cómo mover la posición del cursor de un [DocumentBuilder](../) a un nodo especificado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Run 1. ");

// El constructor de documentos tiene un cursor, que actúa como la parte del documento
// donde el constructor agrega nuevos nodos cuando usamos sus métodos de construcción de documentos.
// Este cursor funciona de la misma manera que el cursor intermitente de Microsoft Word,
// y también siempre termina inmediatamente después de cualquier nodo que el constructor acaba de insertar.
// Para agregar contenido a una parte diferente del documento,
// podemos mover el cursor a un nodo diferente con el método "MoveTo".
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

// El cursor ahora está delante del nodo al que lo movimos.
// Agregar una segunda ejecución lo insertará delante de la primera ejecución.
builder->Writeln(u"Run 2. ");

ASSERT_EQ(u"Run 2. \rRun 1.", doc->GetText().Trim());

// Mueva el cursor al final del documento para continuar agregando texto al final como antes.
builder->MoveTo(doc->get_LastSection()->get_Body()->get_LastParagraph());
builder->Writeln(u"Run 3. ");

ASSERT_EQ(u"Run 2. \rRun 1. \rRun 3.", doc->GetText().Trim());
```

## Ver también

* Class [Node](../../node/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
