---
title: "Clase Aspose::Words::Markup::StructuredDocumentTagCollection"
linktitle: "StructuredDocumentTagCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Markup::StructuredDocumentTagCollection. Una colección de instancias IStructuredDocumentTag que representan las etiquetas de documento estructurado en el rango especificado. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class


Una colección de [IStructuredDocumentTag](../istructureddocumenttag/) instancias que representan las etiquetas de documento estructurado en el rango especificado. Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTagCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Count](./get_count/)() | Devuelve el número de etiquetas de documento estructurado en la colección. |
| [GetById](./getbyid/)(int32_t) | Devuelve la etiqueta de documento estructurado por identificador. |
| [GetByTag](./getbytag/)(const System::String\&) | Devuelve la primera etiqueta de documento estructurado encontrada en la colección con la etiqueta especificada. |
| [GetByTitle](./getbytitle/)(const System::String\&) | Devuelve la primera etiqueta de documento estructurado encontrada en la colección con el título especificado. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Devuelve la etiqueta de documento estructurado en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Elimina la etiqueta de documento estructurado con el identificador especificado. |
| [RemoveAt](./removeat/)(int32_t) | Elimina una etiqueta de documento estructurado en el índice especificado. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
