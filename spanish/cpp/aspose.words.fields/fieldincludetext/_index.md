---
title: "Aspose::Words::Fields::FieldIncludeText clase"
linktitle: "FieldIncludeText"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldIncludeText clase. Implementa el campo INCLUDETEXT. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 58000
url: /es/cpp/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class


Implementa el campo INCLUDETEXT. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldIncludeText : public Aspose::Words::Fields::Field,
                         public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                         public Aspose::Words::Fields::IFieldIncludeTextCode
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() override | Obtiene el nombre del marcador en el documento a incluir. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_Encoding](./get_encoding/)() | Obtiene la codificación aplicada a los datos dentro del archivo referenciado. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_LockFields](./get_lockfields/)() override | Obtiene si se deben impedir que los campos en el documento incluido se actualicen. |
| [get_MimeType](./get_mimetype/)() | Obtiene el tipo MIME del archivo referenciado. |
| [get_NamespaceMappings](./get_namespacemappings/)() override | Obtiene los mapeos de espacio de nombres para consultas XPath. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_Separator](../field/get_separator/)() | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_SourceFullName](./get_sourcefullname/)() override | Obtiene la ubicación del documento usando un IRI. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_TextConverter](./get_textconverter/)() override | Obtiene el nombre del convertidor de texto para el formato del archivo incluido. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [get_XPath](./get_xpath/)() override | Obtiene XPath para la porción deseada del archivo XML. |
| [get_XslTransformation](./get_xsltransformation/)() override | Obtiene la ubicación de la Transformación XSL para formatear datos XML. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Establece el nombre del marcador en el documento a incluir. |
| [set_Encoding](./set_encoding/)(const System::String\&) | Establece la codificación aplicada a los datos dentro del archivo referenciado. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_LockFields](./set_lockfields/)(bool) | Establece si se deben impedir que los campos en el documento incluido se actualicen. |
| [set_MimeType](./set_mimetype/)(const System::String\&) | Establece el tipo MIME del archivo referenciado. |
| [set_NamespaceMappings](./set_namespacemappings/)(const System::String\&) | Establece los mapeos de espacio de nombres para consultas XPath. |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Establece la ubicación del documento usando un IRI. |
| [set_TextConverter](./set_textconverter/)(const System::String\&) | Establece el nombre del conversor de texto para el formato del archivo incluido. |
| [set_XPath](./set_xpath/)(const System::String\&) | Establece XPath para la porción deseada del archivo XML. |
| [set_XslTransformation](./set_xsltransformation/)(const System::String\&) | Establece la ubicación de la transformación XSL para formatear los datos XML. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |
## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
