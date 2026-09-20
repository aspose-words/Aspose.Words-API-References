---
title: "Aspose::Words::Fields::FieldRef clase"
linktitle: "FieldRef"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldRef clase. Implementa el campo REF. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 85000
url: /es/cpp/aspose.words.fields/fieldref/
---
## FieldRef class


Implementa el campo REF. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldRef : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                 public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Obtiene o establece el nombre del marcador referenciado. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_End](./get_end/)() override | Obtiene el nodo que representa el final del campo. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_IncludeNoteOrComment](./get_includenoteorcomment/)() | Obtiene si se deben incrementar los números de nota al pie, nota al final y anotación que están marcados por el marcador, e insertar el texto correspondiente de nota al pie, nota al final y comentario. |
| [get_InsertHyperlink](./get_inserthyperlink/)() | Obtiene si se debe crear un hipervínculo al párrafo marcado. |
| [get_InsertParagraphNumber](./get_insertparagraphnumber/)() | Obtiene si se debe insertar el número de párrafo del párrafo referenciado exactamente como aparece en el documento. |
| [get_InsertParagraphNumberInFullContext](./get_insertparagraphnumberinfullcontext/)() | Obtiene si se debe insertar el número de párrafo del párrafo referenciado en contexto completo. |
| [get_InsertParagraphNumberInRelativeContext](./get_insertparagraphnumberinrelativecontext/)() | Obtiene si se debe insertar el número de párrafo del párrafo referenciado en contexto relativo. |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | Obtiene si se debe insertar la posición relativa del párrafo referenciado. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_NumberSeparator](./get_numberseparator/)() | Obtiene la secuencia de caracteres que se usa para separar los números de secuencia y los números de página. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_Separator](./get_separator/)() override | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_Start](./get_start/)() override | Obtiene el nodo que representa el inicio del campo. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_SuppressNonDelimiters](./get_suppressnondelimiters/)() | Obtiene si se deben suprimir los caracteres que no son delimitadores. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldRef::get_BookmarkName](./get_bookmarkname/). |
| [set_IncludeNoteOrComment](./set_includenoteorcomment/)(bool) | Establece si se deben incrementar los números de nota al pie, nota al final y anotación que están marcados por el marcador, e insertar el texto correspondiente de nota al pie, nota al final y comentario. |
| [set_InsertHyperlink](./set_inserthyperlink/)(bool) | Establece si se debe crear un hipervínculo al párrafo marcado. |
| [set_InsertParagraphNumber](./set_insertparagraphnumber/)(bool) | Establece si se debe insertar el número de párrafo del párrafo referenciado exactamente como aparece en el documento. |
| [set_InsertParagraphNumberInFullContext](./set_insertparagraphnumberinfullcontext/)(bool) | Establece si se debe insertar el número de párrafo del párrafo referenciado en contexto completo. |
| [set_InsertParagraphNumberInRelativeContext](./set_insertparagraphnumberinrelativecontext/)(bool) | Establece si se inserta el número de párrafo del párrafo referenciado en contexto relativo. |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | Establece si se inserta la posición relativa del párrafo referenciado. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NumberSeparator](./set_numberseparator/)(const System::String\&) | Establece la secuencia de caracteres que se usa para separar los números de secuencia y los números de página. |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SuppressNonDelimiters](./set_suppressnondelimiters/)(bool) | Establece si se suprimen los caracteres que no son delimitadores. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |

## Ejemplos



Muestra cómo crear texto marcado con un campo SET y luego mostrarlo en el documento usando un campo REF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nombra el texto marcado con un campo SET.
// Este campo se refiere al "bookmark" no a una estructura de marcador que aparece dentro del texto, sino a una variable con nombre.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// Refiérase al marcador por su nombre en un campo REF y muestre su contenido.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
