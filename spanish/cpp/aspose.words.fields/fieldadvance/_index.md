---
title: "Clase Aspose::Words::Fields::FieldAdvance"
linktitle: "FieldAdvance"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Fields::FieldAdvance. Implementa el campo ADVANCE. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.fields/fieldadvance/
---
## FieldAdvance class


Implementa el campo ADVANCE. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldAdvance : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_DownOffset](./get_downoffset/)() | Obtiene o establece el número de puntos por los que el texto que sigue al campo debe moverse hacia abajo. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_HorizontalPosition](./get_horizontalposition/)() | Obtiene o establece el número de puntos por los que el texto que sigue al campo debe moverse horizontalmente desde el borde izquierdo de la columna, marco o cuadro de texto. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LeftOffset](./get_leftoffset/)() | Obtiene o establece el número de puntos por los que el texto que sigue al campo debe moverse a la izquierda. |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_RightOffset](./get_rightoffset/)() | Obtiene o establece el número de puntos por los que el texto que sigue al campo debe moverse a la derecha. |
| [get_Separator](../field/get_separator/)() | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [get_UpOffset](./get_upoffset/)() | Obtiene o establece el número de puntos por los que el texto que sigue al campo debe moverse hacia arriba. |
| [get_VerticalPosition](./get_verticalposition/)() | Obtiene o establece el número de puntos por los que el texto que sigue al campo debe moverse verticalmente desde el borde superior de la página. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_DownOffset](./set_downoffset/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldAdvance::get_DownOffset](./get_downoffset/). |
| [set_HorizontalPosition](./set_horizontalposition/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldAdvance::get_HorizontalPosition](./get_horizontalposition/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LeftOffset](./set_leftoffset/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldAdvance::get_LeftOffset](./get_leftoffset/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_RightOffset](./set_rightoffset/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldAdvance::get_RightOffset](./get_rightoffset/). |
| [set_UpOffset](./set_upoffset/)(const System::String\&) | Método set para [Aspose::Words::Fields::FieldAdvance::get_UpOffset](./get_upoffset/). |
| [set_VerticalPosition](./set_verticalposition/)(const System::String\&) | Establecedor de [Aspose::Words::Fields::FieldAdvance::get_VerticalPosition](./get_verticalposition/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |

## Ejemplos



Muestra cómo insertar un campo ADVANCE y editar sus propiedades.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This text is in its normal place.");

// A continuación se presentan dos formas de usar el campo ADVANCE para ajustar la posición del texto que le sigue.
// Los efectos de un campo ADVANCE continúan aplicándose hasta que finaliza el párrafo,
// o otro campo ADVANCE actualiza los valores de desplazamiento/coordenadas.
// 1 -  Especifique un desplazamiento direccional:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_RightOffset(u"5");
field->set_UpOffset(u"5");

ASSERT_EQ(u" ADVANCE  \\r 5 \\u 5", field->GetFieldCode());

builder->Write(u"This text will be moved up and to the right.");

field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_DownOffset(u"5");
field->set_LeftOffset(u"100");

ASSERT_EQ(u" ADVANCE  \\d 5 \\l 100", field->GetFieldCode());

builder->Writeln(u"This text is moved down and to the left, overlapping the previous text.");

// 2 -  Mueva el texto a una posición especificada por coordenadas:
field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_HorizontalPosition(u"-100");
field->set_VerticalPosition(u"200");

ASSERT_EQ(u" ADVANCE  \\x -100 \\y 200", field->GetFieldCode());

builder->Write(u"This text is in a custom position.");

doc->Save(get_ArtifactsDir() + u"Field.ADVANCE.docx");
```

## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
