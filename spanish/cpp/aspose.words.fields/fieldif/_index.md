---
title: "Aspose::Words::Fields::FieldIf clase"
linktitle: "FieldIf"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldIf clase. Implementa el campo IF. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 54000
url: /es/cpp/aspose.words.fields/fieldif/
---
## FieldIf class


Implementa el campo IF. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldIf : public Aspose::Words::Fields::Field,
                public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Métodos

| Método | Descripción |
| --- | --- |
| [EvaluateCondition](./evaluatecondition/)() | Evalúa la condición. |
| [get_ComparisonOperator](./get_comparisonoperator/)() | Obtiene o establece el operador de comparación. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtiene el texto que representa el resultado del campo mostrado. |
| [get_End](./get_end/)() override | Obtiene el nodo que representa el final del campo. |
| [get_End](../field/get_end/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FalseText](./get_falsetext/)() | Obtiene o establece el texto mostrado si la expresión de comparación es **false**. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtiene el nodo que representa el final del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_Format](../field/get_format/)() | Obtiene un objeto [FieldFormat](../fieldformat/) que proporciona acceso tipado al formato del campo. |
| [get_IsDirty](../field/get_isdirty/)() | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [get_IsLocked](../field/get_islocked/)() | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [get_LeftExpression](./get_leftexpression/)() | Obtiene o establece la parte izquierda de la expresión de comparación. |
| [get_LocaleId](../field/get_localeid/)() | Obtiene o establece el LCID del campo. |
| [get_Result](../field/get_result/)() | Obtiene o establece el texto que está entre el separador del campo y el final del campo. |
| [get_RightExpression](./get_rightexpression/)() | Obtiene o establece la parte derecha de la expresión de comparación. |
| [get_Separator](./get_separator/)() override | Obtiene el nodo que representa el separador del campo. Puede ser **null**. |
| [get_Start](./get_start/)() override | Obtiene el nodo que representa el inicio del campo. |
| [get_Start](../field/get_start/)() const | Obtiene el nodo que representa el inicio del campo. |
| [get_TrueText](./get_truetext/)() | Obtiene o establece el texto mostrado si la expresión de comparación es true. |
| virtual [get_Type](../field/get_type/)() const | Obtiene el tipo de campo de Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**. |
| [set_ComparisonOperator](./set_comparisonoperator/)(const System::String\&) | Método setter para [Aspose::Words::Fields::FieldIf::get_ComparisonOperator](./get_comparisonoperator/). |
| [set_FalseText](./set_falsetext/)(const System::String\&) | Setter de [Aspose::Words::Fields::FieldIf::get_FalseText](./get_falsetext/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Método set para [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LeftExpression](./set_leftexpression/)(const System::String\&) | Setter de [Aspose::Words::Fields::FieldIf::get_LeftExpression](./get_leftexpression/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Método set para [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Método set para [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_RightExpression](./set_rightexpression/)(const System::String\&) | Setter de [Aspose::Words::Fields::FieldIf::get_RightExpression](./get_rightexpression/). |
| [set_TrueText](./set_truetext/)(const System::String\&) | Setter de [Aspose::Words::Fields::FieldIf::get_TrueText](./get_truetext/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Ejecuta la desvinculación del campo. |
| [Update](../field/update/)() | Ejecuta la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado. |
| [Update](../field/update/)(bool) | Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado. |
## Observaciones


Compara los valores designados por las expresiones [LeftExpression](./get_leftexpression/) y [RightExpression](./get_rightexpression/) en la comparación usando el operador designado por [ComparisonOperator](./get_comparisonoperator/).

Un campo en el siguiente formato se utilizará como origen de combinación de correspondencia: { IF 0 = 0 \"{PatientsNameFML}\" \"\" \\* MERGEFORMAT }

## Ejemplos



Muestra cómo insertar un campo IF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Statement 1: ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"0");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"1");

// El campo IF mostrará una cadena de su propiedad "TrueText",
// o su propiedad "FalseText", dependiendo de la veracidad de la declaración que hemos construido.
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// En este caso, "0 = 1" es incorrecto, por lo que el resultado mostrado será "False".
ASSERT_EQ(u" IF  0 = 1 True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::False, field->EvaluateCondition());
ASSERT_EQ(u"False", field->get_Result());

builder->Write(u"\nStatement 2: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// Esta vez la declaración es correcta, por lo que el resultado mostrado será "True".
ASSERT_EQ(u" IF  5 = \"2 + 3\" True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::True, field->EvaluateCondition());
ASSERT_EQ(u"True", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IF.docx");
```

## Ver también

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
