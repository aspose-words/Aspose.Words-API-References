---
title: "Método Aspose::Words::Fields::Field::get_Result"
linktitle: "get_Result"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::Field::get_Result. Obtiene o establece el texto que está entre el separador del campo y el final del campo en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.fields/field/get_result/
---
## Field::get_Result method


Obtiene o establece el texto que está entre el separador del campo y el final del campo.

```cpp
System::String Aspose::Words::Fields::Field::get_Result()
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

## Ver también

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
