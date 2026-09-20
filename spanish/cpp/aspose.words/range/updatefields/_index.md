---
title: "Método Aspose::Words::Range::UpdateFields"
linktitle: "UpdateFields"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Range::UpdateFields. Actualiza los valores de los campos del documento en este rango en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words/range/updatefields/
---
## Range::UpdateFields method


Actualiza los valores de los campos del documento en este rango.

```cpp
void Aspose::Words::Range::UpdateFields()
```

## Observaciones


Cuando abres, modificas y luego guardas un documento, Aspose.Words no actualiza los campos automáticamente, los mantiene intactos. Por lo tanto, normalmente querrías llamar a este método antes de guardar si has modificado el documento programáticamente y deseas asegurarte de que los valores de campo correctos (calculados) aparezcan en el documento guardado.

No es necesario actualizar los campos después de ejecutar una combinación de correspondencia porque la combinación de correspondencia es un tipo de actualización de campos y actualiza automáticamente todos los campos del documento.

Este método no actualiza todos los tipos de campos. Para la lista detallada de tipos de campos compatibles, consulta la Guía del Programador.

Este método no actualiza los campos que están relacionados con los algoritmos de diseño de página (p. ej., PAGE, PAGES, PAGEREF). Los campos relacionados con el diseño de página se actualizan cuando renderiza un documento o llama a [UpdatePageLayout](../../document/updatepagelayout/).

Para actualizar los campos en todo el documento, use [UpdateFields](../../document/updatefields/).

## Ejemplos



Muestra cómo actualizar todos los campos en un rango.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DOCPROPERTY Category");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->InsertField(u" DOCPROPERTY Category");

// Los campos DOCPROPERTY anteriores mostrarán el valor de esta propiedad de documento incorporada.
doc->get_BuiltInDocumentProperties()->set_Category(u"MyCategory");

// Si actualizamos el valor de una propiedad de documento, necesitaremos actualizar todos los campos DOCPROPERTY para que lo muestren.
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Actualice todos los campos que están en el rango de la primera sección.
doc->get_FirstSection()->get_Range()->UpdateFields();

ASSERT_EQ(u"MyCategory", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
```

## Ver también

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
