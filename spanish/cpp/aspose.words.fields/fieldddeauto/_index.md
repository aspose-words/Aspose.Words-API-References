---
title: "Aspose::Words::Fields::FieldDdeAuto clase"
linktitle: "FieldDdeAuto"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldDdeAuto clase. Implementa el campo DDEAUTO. Para obtener más información, visita el artículo de documentación en C++."
type: docs
weight: 33000
url: /es/cpp/aspose.words.fields/fieldddeauto/
---
## FieldDdeAuto class


Implementa el campo DDEAUTO. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldDdeAuto : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_InsertAsBitmap](./get_insertasbitmap/)() | Obtiene si se debe insertar el objeto vinculado como un mapa de bits. |
| [get_InsertAsHtml](./get_insertashtml/)() | Obtiene si se debe insertar el objeto vinculado como texto con formato HTML. |
| [get_InsertAsPicture](./get_insertaspicture/)() | Obtiene si se debe insertar el objeto vinculado como una imagen. |
| [get_InsertAsRtf](./get_insertasrtf/)() | Obtiene si se debe insertar el objeto vinculado en formato de texto enriquecido (RTF). |
| [get_InsertAsText](./get_insertastext/)() | Obtiene si se debe insertar el objeto vinculado en formato solo de texto. |
| [get_InsertAsUnicode](./get_insertasunicode/)() | Obtiene si se debe insertar el objeto vinculado como texto Unicode. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLinked](./get_islinked/)() | Obtiene si se debe reducir el tamaño del archivo al no almacenar datos gráficos con el documento. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_ProgId](./get_progid/)() | Obtiene el tipo de aplicación de la información del enlace. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_Separator](../field/get_separator/)() | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_SourceFullName](./get_sourcefullname/)() | Obtiene el nombre y la ubicación del archivo fuente. |
| [get_SourceItem](./get_sourceitem/)() | Obtiene la parte del archivo fuente que se está vinculando. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_InsertAsBitmap](./set_insertasbitmap/)(bool) | Establece si se debe insertar el objeto vinculado como un mapa de bits. |
| [set_InsertAsHtml](./set_insertashtml/)(bool) | Establece si se debe insertar el objeto vinculado como texto con formato HTML. |
| [set_InsertAsPicture](./set_insertaspicture/)(bool) | Establece si se debe insertar el objeto vinculado como una imagen. |
| [set_InsertAsRtf](./set_insertasrtf/)(bool) | Establece si se debe insertar el objeto vinculado en formato de texto enriquecido (RTF). |
| [set_InsertAsText](./set_insertastext/)(bool) | Establece si se debe insertar el objeto vinculado en formato solo de texto. |
| [set_InsertAsUnicode](./set_insertasunicode/)(bool) | Establece si se debe insertar el objeto enlazado como texto Unicode. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLinked](./set_islinked/)(bool) | Establece si se debe reducir el tamaño del archivo al no almacenar datos gráficos con el documento. |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ProgId](./set_progid/)(const System::String\&) | Establece el tipo de aplicación de la información del enlace. |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Establece el nombre y la ubicación del archivo fuente. |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | Establece la parte del archivo fuente que se está enlazando. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |
## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
