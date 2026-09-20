---
title: "Aspose::Words::Fields::FieldToa clase"
linktitle: "FieldToa"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldToa clase. Implementa el campo TOA. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 104000
url: /es/cpp/aspose.words.fields/fieldtoa/
---
## FieldToa class


Implementa el campo TOA. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldToa : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Obtiene el nombre del marcador que indica la parte del documento utilizada para crear la tabla. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_EntryCategory](./get_entrycategory/)() | Obtiene la categoría integral para las entradas incluidas en la tabla. |
| [get_EntrySeparator](./get_entryseparator/)() | Obtiene la secuencia de caracteres que se usa para separar una entrada de tabla de autoridades y su número de página. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | Obtiene la secuencia de caracteres que se usa para separar dos números de página en una lista de números de página. |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | Obtiene la secuencia de caracteres que se usa para separar el inicio y el fin de un rango de páginas. |
| [get_RemoveEntryFormatting](./get_removeentryformatting/)() | Obtiene si se debe eliminar el formato del texto de la entrada en el documento de la entrada en la tabla de autoridades. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_Separator](../field/get_separator/)() | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_SequenceName](./get_sequencename/)() | Obtiene el nombre de una secuencia cuyo número se incluye con el número de página. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Obtiene la secuencia de caracteres que se usa para separar los números de secuencia y los números de página. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [get_UseHeading](./get_useheading/)() | Obtiene si se debe incluir el encabezado de categoría para las entradas en una tabla de autoridades. |
| [get_UsePassim](./get_usepassim/)() | Obtiene si se deben reemplazar cinco o más referencias de página diferentes a la misma autoridad con "passim", que se usa para indicar que una palabra o pasaje ocurre frecuentemente en la obra citada. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Establece el nombre del marcador que indica la parte del documento utilizada para crear la tabla. |
| [set_EntryCategory](./set_entrycategory/)(const System::String\&) | Establece la categoría integral para las entradas incluidas en la tabla. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Establece la secuencia de caracteres que se usa para separar una entrada de tabla de autoridades y su número de página. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | Establece la secuencia de caracteres que se usa para separar dos números de página en una lista de números de página. |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | Establece la secuencia de caracteres que se usa para separar el inicio y el fin de un rango de páginas. |
| [set_RemoveEntryFormatting](./set_removeentryformatting/)(bool) | Establece si se debe eliminar el formato del texto de la entrada en el documento de la entrada en la tabla de autoridades. |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | Establece el nombre de una secuencia cuyo número se incluye con el número de página. |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Establece la secuencia de caracteres que se usa para separar los números de secuencia y los números de página. |
| [set_UseHeading](./set_useheading/)(bool) | Establece si se debe incluir el encabezado de categoría para las entradas en una tabla de autoridades. |
| [set_UsePassim](./set_usepassim/)(bool) | Establece si se deben reemplazar cinco o más referencias de página diferentes a la misma autoridad con "passim", que se utiliza para indicar que una palabra o pasaje aparece con frecuencia en la obra citada. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |
## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
