---
title: "Método Aspose::Words::DocumentBuilder::MoveToBookmark"
linktitle: "MoveToBookmark"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBuilder::MoveToBookmark. Mueve el cursor a un marcador en C++."
type: docs
weight: 52000
url: /es/cpp/aspose.words/documentbuilder/movetobookmark/
---
## DocumentBuilder::MoveToBookmark(const System::String\&) method


Mueve el cursor a un marcador.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| bookmarkName | const System::String\& | El nombre del marcador al que mover el cursor. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## Observaciones


Mueve el cursor a una posición justo después del inicio del marcador con el nombre especificado.

La comparación no distingue entre mayúsculas y minúsculas. Si no se encuentra el marcador, se devuelve **false** y el cursor no se mueve.

Insertar texto nuevo no reemplaza el texto existente del marcador.

Tenga en cuenta que algunos marcadores en el documento están asignados a campos de formulario. Moverse a dicho marcador e insertar texto allí inserta el texto en el código del campo de formulario. Aunque esto no invalidará el campo de formulario, el texto insertado no será visible porque pasa a ser parte del código del campo.

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

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToBookmark(const System::String\&, bool, bool) method


Mueve el cursor a un marcador con mayor precisión.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName, bool isStart, bool isAfter)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| bookmarkName | const System::String\& | El nombre del marcador al que mover el cursor. |
| isStart | bool | Cuando **true**, mueve el cursor al comienzo del marcador. Cuando **false**, mueve el cursor al final del marcador. |
| isAfter | bool | Cuando **true**, mueve el cursor para que esté después de la posición de inicio o fin del marcador. Cuando **false**, mueve el cursor para que esté antes de la posición de inicio o fin del marcador. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## Observaciones


Mueve el cursor a una posición antes o después del inicio o fin del marcador.

Si la posición deseada no está a nivel en línea, se mueve al siguiente párrafo.

La comparación no distingue entre mayúsculas y minúsculas. Si no se encuentra el marcador, se devuelve **false** y el cursor no se mueve.

## Ejemplos



Muestra cómo mover el cursor del punto de inserción de nodos de un DocumentBuilder a un marcador.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un marcador válido consta de un nodo BookmarkStart, un nodo BookmarkEnd con un
// nombre de marcador coincidente en algún punto posterior, y contenido encerrado por esos nodos.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world! ");
builder->EndBookmark(u"MyBookmark");

// Hay 4 formas de mover el cursor de un DocumentBuilder a un marcador.
// Si estamos entre los nodos BookmarkStart y BookmarkEnd, el cursor estará dentro del marcador.
// Esto significa que cualquier texto añadido por el builder se convertirá en parte del marcador.
// 1 -  Fuera del marcador, delante del nodo BookmarkStart:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, false));
builder->Write(u"1. ");

ASSERT_EQ(u"Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. Hello world!", doc->GetText().Trim());

// 2 -  Dentro del marcador, justo después del nodo BookmarkStart:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, true));
builder->Write(u"2. ");

ASSERT_EQ(u"2. Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world!", doc->GetText().Trim());

// 2 -  Dentro del marcador, justo delante del nodo BookmarkEnd:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, false));
builder->Write(u"3. ");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3.", doc->GetText().Trim());

// 4 -  Fuera del marcador, después del nodo BookmarkEnd:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, true));
builder->Write(u"4.");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3. 4.", doc->GetText().Trim());
```

## Ver también

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
