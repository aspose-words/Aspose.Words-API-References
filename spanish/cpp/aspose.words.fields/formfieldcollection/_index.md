---
title: "Clase Aspose::Words::Fields::FormFieldCollection"
linktitle: "FormFieldCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Fields::FormFieldCollection. Una colección de objetos FormField que representan todos los campos de formulario en un rango. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 113000
url: /es/cpp/aspose.words.fields/formfieldcollection/
---
## FormFieldCollection class


Una colección de objetos [FormField](../formfield/) que representan todos los campos de formulario en un rango. Para obtener más información, visite el artículo de documentación [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/).

```cpp
class FormFieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::FormField>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Clear](./clear/)() | Elimina todos los campos de formulario de esta colección y del documento. |
| [get_Count](./get_count/)() | Devuelve el número de campos de formulario en la colección. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Devuelve un campo de formulario en el índice especificado. |
| [idx_get](./idx_get/)(const System::String\&) | Devuelve un campo de formulario por nombre de marcador. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Elimina un campo de formulario con el nombre especificado. |
| [RemoveAt](./removeat/)(int32_t) | Elimina un campo de formulario en el índice especificado. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
