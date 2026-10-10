---
title: "Aspose::Words::Range::NormalizeFieldTypes método"
linktitle: "NormalizeFieldTypes"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Range::NormalizeFieldTypes method. Cambia los valores del tipo de campo FieldType de FieldStart, FieldSeparator y FieldEnd en este rango para que correspondan con los tipos de campo contenidos en los códigos de campo en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words/range/normalizefieldtypes/
---
## Range::NormalizeFieldTypes method


Cambia los valores del tipo de campo [FieldType](../../../aspose.words.fields/fieldchar/get_fieldtype/) de [FieldStart](../../../aspose.words.fields/fieldstart/), [FieldSeparator](../../../aspose.words.fields/fieldseparator/) y [FieldEnd](../../../aspose.words.fields/fieldend/) en este rango para que correspondan con los tipos de campo contenidos en los códigos de campo.

```cpp
void Aspose::Words::Range::NormalizeFieldTypes()
```

## Observaciones


Utiliza este método después de cambios en el documento que afecten a los tipos de campo.

Para cambiar los valores del tipo de campo en todo el documento, use [NormalizeFieldTypes](../../document/normalizefieldtypes/).

## Ejemplos



Muestra cómo mantener actualizado el tipo de un campo con su código de campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE", nullptr);

// Aspose.Words detecta automáticamente los tipos de campo basándose en los códigos de campo.
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());

// Cambia manualmente el texto sin formato del campo, que determina el código del campo.
auto fieldText = System::ExplicitCast<Aspose::Words::Run>(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(0));
fieldText->set_Text(u"PAGE");

// Cambiar el código del campo ha convertido este campo en uno de tipo diferente,
// pero las propiedades de tipo del campo siguen mostrando el tipo anterior.
ASSERT_EQ(u"PAGE", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_End()->get_FieldType());

// Actualiza esas propiedades con este método para mostrar el valor actual.
doc->NormalizeFieldTypes();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_End()->get_FieldType());
```

## Ver también

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
