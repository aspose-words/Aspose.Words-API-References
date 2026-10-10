---
title: "Clase Aspose::Words::Fields::FieldNumPages"
linktitle: "FieldNumPages"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Fields::FieldNumPages. Implementa el campo NUMPAGES. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 74000
url: /es/cpp/aspose.words.fields/fieldnumpages/
---
## FieldNumPages class


Implementa el campo NUMPAGES. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldNumPages : public Aspose::Words::Fields::Field
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_Separator](../field/get_separator/)() | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |

## Ejemplos



Muestra cómo usar los campos NUMCHARS, NUMWORDS, NUMPAGES y PAGE para rastrear el tamaño de nuestros documentos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

// A continuación se presentan tres tipos de campos que podemos usar para rastrear el tamaño de nuestros documentos.
// 1 -  Rastrear el recuento de caracteres con un campo NUMCHARS:
auto fieldNumChars = System::ExplicitCast<Aspose::Words::Fields::FieldNumChars>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldNumChars, true));
builder->Writeln(u" characters");

// 2 -  Rastrear el recuento de palabras con un campo NUMWORDS:
auto fieldNumWords = System::ExplicitCast<Aspose::Words::Fields::FieldNumWords>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldNumWords, true));
builder->Writeln(u" words");

// 3 -  Utilizar los campos PAGE y NUMPAGES para mostrar en qué página está el campo,
// y el número total de páginas en el documento:
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);
builder->Write(u"Page ");
auto fieldPage = System::ExplicitCast<Aspose::Words::Fields::FieldPage>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPage, true));
builder->Write(u" of ");
auto fieldNumPages = System::ExplicitCast<Aspose::Words::Fields::FieldNumPages>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldNumPages, true));

ASSERT_EQ(u" NUMCHARS ", fieldNumChars->GetFieldCode());
ASSERT_EQ(u" NUMWORDS ", fieldNumWords->GetFieldCode());
ASSERT_EQ(u" NUMPAGES ", fieldNumPages->GetFieldCode());
ASSERT_EQ(u" PAGE ", fieldPage->GetFieldCode());

// Estos campos no mantendrán valores precisos en tiempo real
// mientras editamos el documento programáticamente usando Aspose.Words, o en Microsoft Word.
// Necesitamos actualizarlos cada vez que necesitemos ver un valor actualizado.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.NUMCHARS.NUMWORDS.NUMPAGES.PAGE.docx");
```

## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
