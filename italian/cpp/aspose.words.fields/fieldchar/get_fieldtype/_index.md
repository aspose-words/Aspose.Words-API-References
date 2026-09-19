---
title: "Metodo Aspose::Words::Fields::FieldChar::get_FieldType"
linktitle: "get_FieldType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldChar::get_FieldType. Restituisce il tipo del campo in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldchar/get_fieldtype/
---
## FieldChar::get_FieldType method


Restituisce il tipo del campo.

```cpp
Aspose::Words::Fields::FieldType Aspose::Words::Fields::FieldChar::get_FieldType() const
```


## Esempi



Mostra come lavorare con un nodo [FieldStart](../../fieldstart/).
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

// Recupera l'oggetto facciata che rappresenta il campo nel documento.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(false, field->get_IsLocked());
ASSERT_EQ(u" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Aggiorna il campo per mostrare la data corrente.
field->Update();
```

## Vedi anche

* Enum [FieldType](../../fieldtype/)
* Class [FieldChar](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
