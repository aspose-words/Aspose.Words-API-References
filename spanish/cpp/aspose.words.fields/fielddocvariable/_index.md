---
title: "clase Aspose::Words::Fields::FieldDocVariable"
linktitle: "FieldDocVariable"
second_title: "Referencia de API de Aspose.Words para C++"
description: "clase Aspose::Words::Fields::FieldDocVariable. Implementa el campo DOCVARIABLE. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 36000
url: /es/cpp/aspose.words.fields/fielddocvariable/
---
## FieldDocVariable class


Implementa el campo DOCVARIABLE. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldDocVariable : public Aspose::Words::Fields::Field
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
| [get_VariableName](./get_variablename/)() | Obtiene o establece el nombre de la variable del documento a recuperar. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_VariableName](./set_variablename/)(const System::String\&) | Establecedor para [Aspose::Words::Fields::FieldDocVariable::get_VariableName](./get_variablename/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |

## Ejemplos



Muestra cómo usar campos DOCPROPERTY para mostrar propiedades del documento y variables.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan dos formas de usar campos DOCPROPERTY.
// 1 -  Mostrar una propiedad incorporada:
// Establezca un valor personalizado para la propiedad incorporada "Category", luego inserte un campo DOCPROPERTY que lo referencie.
doc->get_BuiltInDocumentProperties()->set_Category(u"My category");

auto fieldDocProperty = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY Category "));
fieldDocProperty->Update();

ASSERT_EQ(u" DOCPROPERTY Category ", fieldDocProperty->GetFieldCode());
ASSERT_EQ(u"My category", fieldDocProperty->get_Result());

builder->InsertParagraph();

// 2 -  Mostrar una variable de documento personalizada:
// Defina una variable personalizada, luego haga referencia a esa variable con un campo DOCPROPERTY.
ASSERT_EQ(0, doc->get_Variables()->get_Count());
doc->get_Variables()->Add(u"My variable", u"My variable's value");

auto fieldDocVariable = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
fieldDocVariable->set_VariableName(u"My Variable");
fieldDocVariable->Update();

ASSERT_EQ(u" DOCVARIABLE  \"My Variable\"", fieldDocVariable->GetFieldCode());
ASSERT_EQ(u"My variable's value", fieldDocVariable->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.DOCPROPERTY.DOCVARIABLE.docx");
```

## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
