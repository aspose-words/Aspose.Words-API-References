---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection método"
linktitle: "get_IsMultiSection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection. Devuelve true si esta instancia es una etiqueta de documento estructurado con rango (multi‑sección) en C++."
type: docs
weight: 3500
url: /es/cpp/aspose.words.markup/istructureddocumenttag/get_ismultisection/
---
## IStructuredDocumentTag::get_IsMultiSection method


Devuelve true si esta instancia es una etiqueta de documento estructurado con rango (multi sección).

```cpp
virtual bool Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection()=0
```


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

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
