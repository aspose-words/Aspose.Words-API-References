---
title: "Aspose::Words::Fields::FieldChar::get_IsDirty método"
linktitle: "get_IsDirty"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldChar::get_IsDirty método. Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.fields/fieldchar/get_isdirty/
---
## FieldChar::get_IsDirty method


Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento.

```cpp
bool Aspose::Words::Fields::FieldChar::get_IsDirty() const
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

* Class [FieldChar](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
