---
title: "Método Aspose::Words::Range::get_StructuredDocumentTags"
linktitle: "get_StructuredDocumentTags"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Range::get_StructuredDocumentTags. Devuelve una colección StructuredDocumentTags que representa todas las etiquetas de documento estructurado en el rango en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words/range/get_structureddocumenttags/
---
## Range::get_StructuredDocumentTags method


Devuelve una colección [StructuredDocumentTags](./) que representa todas las etiquetas de documento estructurado en el rango.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTagCollection> Aspose::Words::Range::get_StructuredDocumentTags()
```


## Ejemplos



Muestra cómo eliminar una etiqueta de documento estructurado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTagCollection> structuredDocumentTags = doc->get_Range()->get_StructuredDocumentTags();
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt;
for (int32_t i = 0; i < structuredDocumentTags->get_Count(); i++)
{
    sdt = structuredDocumentTags->idx_get(i);
    std::cout << sdt->get_Title() << std::endl;
}

sdt = structuredDocumentTags->GetById(1691867797);
ASSERT_EQ(1691867797, sdt->get_Id());

ASSERT_EQ(5, structuredDocumentTags->get_Count());
// Elimine la etiqueta de documento estructurado por Id.
structuredDocumentTags->Remove(1691867797);
// Elimine la etiqueta de documento estructurado en la posición 0.
structuredDocumentTags->RemoveAt(0);
ASSERT_EQ(3, structuredDocumentTags->get_Count());
```

## Ver también

* Class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
