---
title: "Método GetFieldCode de Aspose::Words::Fields::Field"
linktitle: "GetFieldCode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método GetFieldCode de Aspose::Words::Fields::Field. Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Tanto el código del campo como el resultado del campo de los campos hijos están incluidos en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.fields/field/getfieldcode/
---
## Field::GetFieldCode() method


Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado de los campos secundarios.

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode()
```


## Ejemplos



Muestra cómo insertar un campo en un documento usando un código de campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Esta sobrecarga del método InsertField actualiza automáticamente los campos insertados.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```


Muestra cómo obtener el código de campo de un campo.
```cpp
// Abra un documento que contenga un MERGEFIELD dentro de un campo IF.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// Hay dos formas de obtener el código de campo de un campo:
// 1 -  Omitir sus campos internos:
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  Incluir sus campos internos:
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// Por defecto, el método GetFieldCode muestra los campos internos.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## Ver también

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## Field::GetFieldCode(bool) method


Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador).

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode(bool includeChildFieldCodes)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| includeChildFieldCodes | bool | **true** si se deben incluir los códigos de campo secundarios. |

## Ejemplos



Muestra cómo obtener el código de campo de un campo.
```cpp
// Abra un documento que contenga un MERGEFIELD dentro de un campo IF.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// Hay dos formas de obtener el código de campo de un campo:
// 1 -  Omitir sus campos internos:
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  Incluir sus campos internos:
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// Por defecto, el método GetFieldCode muestra los campos internos.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## Ver también

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
