---
title: "Método Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle"
linktitle: "GetByTitle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle. Devuelve la primera etiqueta de documento estructurado encontrada en la colección con el título especificado en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection::GetByTitle method


Devuelve la primera etiqueta de documento estructurado encontrada en la colección con el título especificado.

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle(const System::String &title)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| título | const System::String\& | El título de la etiqueta de documento estructurado. |
## Observaciones


Devuelve null si no se puede encontrar la etiqueta de documento estructurado con el título especificado.

## Ejemplos



Muestra cómo obtener la etiqueta de documento estructurado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags by id.docx");

// Obtenga la etiqueta de documento estructurado por Id.
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt = doc->get_Range()->get_StructuredDocumentTags()->GetById(1160505028);
std::cout << System::Convert::ToString(sdt->get_IsMultiSection()) << std::endl;
std::cout << sdt->get_Title() << std::endl;

// Obtenga la etiqueta de documento estructurado o la etiqueta de rango por Título.
sdt = doc->get_Range()->get_StructuredDocumentTags()->GetByTitle(u"Alias4");
std::cout << sdt->get_Id() << std::endl;
```

## Ver también

* Interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
