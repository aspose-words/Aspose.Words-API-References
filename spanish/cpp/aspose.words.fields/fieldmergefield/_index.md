---
title: "Aspose::Words::Fields::FieldMergeField clase"
linktitle: "FieldMergeField"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldMergeField clase. Implementa el campo MERGEFIELD. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 67000
url: /es/cpp/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class


Implementa el campo MERGEFIELD. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldMergeField : public Aspose::Words::Fields::Field,
                        public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldName](./get_fieldname/)() | Obtiene el nombre de un campo de datos. |
| [get_FieldNameNoPrefix](./get_fieldnamenoprefix/)() const | Devuelve solo el nombre del campo de datos. Cualquier prefijo se elimina a la propiedad prefix. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_IsMapped](./get_ismapped/)() | Obtiene si este campo es un campo mapeado. |
| [get_IsVerticalFormatting](./get_isverticalformatting/)() | Obtiene si se debe habilitar la conversión de caracteres para el formato vertical. |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_Separator](../field/get_separator/)() | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_TextAfter](./get_textafter/)() | Obtiene el texto que se insertará después del campo si el campo no está vacío. |
| [get_TextBefore](./get_textbefore/)() | Obtiene el texto que se insertará antes del campo si el campo no está vacío. |
| [get_Type](./get_type/)() const override | Obtiene el tipo de campo de Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_FieldName](./set_fieldname/)(const System::String\&) | Establece el nombre de un campo de datos. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_IsMapped](./set_ismapped/)(bool) | Establece si este campo es un campo mapeado. |
| [set_IsVerticalFormatting](./set_isverticalformatting/)(bool) | Establece si se debe habilitar la conversión de caracteres para el formato vertical. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_TextAfter](./set_textafter/)(const System::String\&) | Establece el texto que se insertará después del campo si el campo no está vacío. |
| [set_TextBefore](./set_textbefore/)(const System::String\&) | Establece el texto que se insertará antes del campo si el campo no está vacío. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |
## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
