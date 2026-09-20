---
title: "Clase Aspose::Words::Fields::FieldFormDropDown"
linktitle: "FieldFormDropDown"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Fields::FieldFormDropDown. Implementa el campo FORMDROPDOWN. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 47000
url: /es/cpp/aspose.words.fields/fieldformdropdown/
---
## FieldFormDropDown class


Implementa el campo FORMDROPDOWN. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldFormDropDown : public Aspose::Words::Fields::Field
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



Muestra cómo procesar los campos FORMCHECKBOX, FORMDROPDOWN y FORMTEXT.
```cpp
// Estos campos son equivalentes heredados de FormField. Podemos leerlos, pero no crear estos campos usando Aspose.Words.
// En Microsoft Word, podemos insertar estos campos a través del menú Herramientas heredadas en la pestaña Desarrollador.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

auto fieldFormCheckBox = System::ExplicitCast<Aspose::Words::Fields::FieldFormCheckBox>(doc->get_Range()->get_Fields()->idx_get(1));
ASSERT_EQ(u" FORMCHECKBOX \u0001", fieldFormCheckBox->GetFieldCode());

auto fieldFormDropDown = System::ExplicitCast<Aspose::Words::Fields::FieldFormDropDown>(doc->get_Range()->get_Fields()->idx_get(2));
ASSERT_EQ(u" FORMDROPDOWN \u0001", fieldFormDropDown->GetFieldCode());

auto fieldFormText = System::ExplicitCast<Aspose::Words::Fields::FieldFormText>(doc->get_Range()->get_Fields()->idx_get(0));
ASSERT_EQ(u" FORMTEXT \u0001", fieldFormText->GetFieldCode());
```

## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
