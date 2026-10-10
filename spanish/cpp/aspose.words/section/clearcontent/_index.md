---
title: "Método Aspose::Words::Section::ClearContent"
linktitle: "ClearContent"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Section::ClearContent. Borra la sección en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/section/clearcontent/
---
## Section::ClearContent method


Borra la sección.

```cpp
void Aspose::Words::Section::ClearContent()
```

## Observaciones


El texto de [Body](../get_body/) se borra, quedando solo un párrafo vacío que representa el salto de sección.

El texto de todos los encabezados y pies de página se borra, pero los objetos [HeaderFooter](../../headerfooter/) en sí no se eliminan.

## Ejemplos



Muestra cómo borrar el contenido de una sección.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Ejecutar el método \"ClearContent\" eliminará todo el contenido de la sección
// pero dejará un párrafo en blanco para volver a agregar contenido.
doc->get_FirstSection()->ClearContent();

ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());
```

## Ver también

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
