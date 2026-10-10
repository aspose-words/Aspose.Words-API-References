---
title: "Método Aspose::Words::Section::get_Body"
linktitle: "get_Body"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Section::get_Body. Devuelve el nodo hijo Body de la sección en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words/section/get_body/
---
## Section::get_Body method


Devuelve el nodo hijo [Body](../../body/) de la sección.

```cpp
System::SharedPtr<Aspose::Words::Body> Aspose::Words::Section::get_Body()
```

## Observaciones


[Body](../../body/) contains main text of the section.

Devuelve **null** si la sección no tiene un nodo [Body](../../body/) entre sus hijos.

## Ejemplos



Borra el texto principal de todas las secciones del documento dejando las propias secciones.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento en blanco contiene una sección, un cuerpo y un párrafo.
// Llame al método "RemoveAllChildren" para eliminar todos esos nodos,
// y termine con un nodo de documento sin hijos.
doc->RemoveAllChildren();

// Este documento ahora no tiene nodos hijos compuestos a los que podamos añadir contenido.
// Si deseamos editarlo, necesitaremos volver a poblar su colección de nodos.
// Primero, cree una nueva sección y luego añádala como hijo al nodo raíz del documento.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido
// en la página entre el encabezado y el pie de página de la sección.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Este cuerpo no tiene hijos, por lo que aún no podemos agregar runs a él.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Llame a "EnsureMinimum" para asegurarse de que este cuerpo contenga al menos un párrafo vacío.
body->EnsureMinimum();

// Ahora, podemos agregar runs al cuerpo y hacer que el documento los muestre.
body->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Ver también

* Class [Body](../../body/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
