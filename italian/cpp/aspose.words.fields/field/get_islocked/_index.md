---
title: "Aspose::Words::Fields::Field::get_IsLocked method"
linktitle: "get_IsLocked"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::Field::get_IsLocked method. Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il risultato) in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.fields/field/get_islocked/
---
## Field::get_IsLocked method


Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato).

```cpp
bool Aspose::Words::Fields::Field::get_IsLocked()
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

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
