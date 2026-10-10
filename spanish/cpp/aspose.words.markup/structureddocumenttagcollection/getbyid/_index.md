---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetById método"
linktitle: "GetById"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetById método. Devuelve la etiqueta de documento estructurado por identificador en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection::GetById method


Devuelve la etiqueta de documento estructurado por identificador.

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetById(int32_t id)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| id | int32_t | El identificador de la etiqueta de documento estructurado. |
## Observaciones


Devuelve null si no se puede encontrar la etiqueta de documento estructurado con el identificador especificado.

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
