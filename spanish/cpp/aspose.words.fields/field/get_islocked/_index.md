---
title: "Aspose::Words::Fields::Field::get_IsLocked method"
linktitle: "get_IsLocked"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::Field::get_IsLocked method. Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado) en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.fields/field/get_islocked/
---
## Field::get_IsLocked method


Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado).

```cpp
bool Aspose::Words::Fields::Field::get_IsLocked()
```


## Ejemplos



Muestra cómo trabajar con un nodo [FieldStart](../../fieldstart/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->get_Format()->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

System::SharedPtr<Aspose::Words::Fields::FieldChar> fieldStart = field->get_Start();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, fieldStart->get_FieldType());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsDirty());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsLocked());

// Recupera el objeto fachada que representa el campo en el documento.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(false, field->get_IsLocked());
ASSERT_EQ(u" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Actualiza el campo para mostrar la fecha actual.
field->Update();
```

## Ver también

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
