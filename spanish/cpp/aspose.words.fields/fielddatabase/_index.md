---
title: "Aspose::Words::Fields::FieldDatabase clase"
linktitle: "FieldDatabase"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldDatabase clase. Implementa el campo DATABASE. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 28000
url: /es/cpp/aspose.words.fields/fielddatabase/
---
## FieldDatabase class


Implementa el campo DATABASE. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldDatabase : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Métodos

| Método | Descripción |
| --- | --- |
| [FieldDatabase](./fielddatabase/)() |  |
| [get_Connection](./get_connection/)() | Obtiene una conexión a los datos. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_FileName](./get_filename/)() | Obtiene la ruta completa y el nombre de archivo de la base de datos. |
| [get_FirstRecord](./get_firstrecord/)() | Obtiene el número entero de registro del primer registro de datos a insertar. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_FormatAttributes](./get_formatattributes/)() | Obtiene qué atributos del formato se aplicarán a la tabla. |
| [get_InsertHeadings](./get_insertheadings/)() | Obtiene si se deben insertar los nombres de campo de la base de datos como encabezados de columna en la tabla resultante. |
| [get_InsertOnceOnMailMerge](./get_insertonceonmailmerge/)() | Obtiene si se deben insertar datos al comienzo de una combinación. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LastRecord](./get_lastrecord/)() | Obtiene el número entero de registro del último registro de datos a insertar. |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_Query](./get_query/)() | Obtiene un conjunto de instrucciones SQL que consultan la base de datos. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_Separator](../field/get_separator/)() | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_TableFormat](./get_tableformat/)() | Obtiene el formato que se aplicará al resultado de la consulta a la base de datos. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_Connection](./set_connection/)(const System::String\&) | Establece una conexión a los datos. |
| [set_FileName](./set_filename/)(const System::String\&) | Establece la ruta completa y el nombre de archivo de la base de datos. |
| [set_FirstRecord](./set_firstrecord/)(const System::String\&) | Establece el número entero de registro del primer registro de datos a insertar. |
| [set_FormatAttributes](./set_formatattributes/)(const System::String\&) | Establece qué atributos del formato se aplicarán a la tabla. |
| [set_InsertHeadings](./set_insertheadings/)(bool) | Establece si se deben insertar los nombres de campo de la base de datos como encabezados de columna en la tabla resultante. |
| [set_InsertOnceOnMailMerge](./set_insertonceonmailmerge/)(bool) | Establece si se deben insertar datos al comienzo de una combinación. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LastRecord](./set_lastrecord/)(const System::String\&) | Establece el número entero de registro del último registro de datos a insertar. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Query](./set_query/)(const System::String\&) | Establece un conjunto de instrucciones SQL que consultan la base de datos. |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_TableFormat](./set_tableformat/)(const System::String\&) | Establece el formato que se aplicará al resultado de la consulta de la base de datos. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |
## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
