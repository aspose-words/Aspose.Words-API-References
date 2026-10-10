---
title: "Aspose::Words::Fields::FieldCitation clase"
linktitle: "FieldCitation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldCitation clase. Implementa el campo CITATION. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 22000
url: /es/cpp/aspose.words.fields/fieldcitation/
---
## FieldCitation class


Implementa el campo CITATION. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldCitation : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_AnotherSourceTag](./get_anothersourcetag/)() | Obtiene un valor que coincide con el valor del elemento **Tag** de otra fuente que se incluirá en la cita. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_FormatLanguageId](./get_formatlanguageid/)() | Obtiene el ID de idioma que se utiliza junto con el estilo bibliográfico especificado para formatear la cita en el documento. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_PageNumber](./get_pagenumber/)() | Obtiene un número de página asociado a la cita. |
| [get_Prefix](./get_prefix/)() | Obtiene un prefijo que se antepone a la cita. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_Separator](../field/get_separator/)() | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_SourceTag](./get_sourcetag/)() | Obtiene un valor que coincide con el valor del elemento **Tag** de la fuente a insertar. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Suffix](./get_suffix/)() | Obtiene un sufijo que se agrega a la cita. |
| [get_SuppressAuthor](./get_suppressauthor/)() | Obtiene si la información del autor está suprimida de la cita. |
| [get_SuppressTitle](./get_suppresstitle/)() | Obtiene si la información del título está suprimida de la cita. |
| [get_SuppressYear](./get_suppressyear/)() | Obtiene si la información del año está suprimida de la cita. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [get_VolumeNumber](./get_volumenumber/)() | Obtiene un número de volumen asociado a la cita. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_AnotherSourceTag](./set_anothersourcetag/)(const System::String\&) | Establece un valor que coincide con el valor del elemento **Tag** de otra fuente que se incluirá en la cita. |
| [set_FormatLanguageId](./set_formatlanguageid/)(const System::String\&) | Establece el ID de idioma que se utiliza junto con el estilo bibliográfico especificado para formatear la cita en el documento. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumber](./set_pagenumber/)(const System::String\&) | Establece un número de página asociado a la cita. |
| [set_Prefix](./set_prefix/)(const System::String\&) | Establece un prefijo que se antepone a la cita. |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceTag](./set_sourcetag/)(const System::String\&) | Establece un valor que coincide con el valor del elemento **Tag** de la fuente a insertar. |
| [set_Suffix](./set_suffix/)(const System::String\&) | Establece un sufijo que se agrega a la cita. |
| [set_SuppressAuthor](./set_suppressauthor/)(bool) | Establece si la información del autor está suprimida de la cita. |
| [set_SuppressTitle](./set_suppresstitle/)(bool) | Establece si la información del título está suprimida de la cita. |
| [set_SuppressYear](./set_suppressyear/)(bool) | Establece si la información del año está suprimida de la cita. |
| [set_VolumeNumber](./set_volumenumber/)(const System::String\&) | Establece un número de volumen asociado a la cita. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |
## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
