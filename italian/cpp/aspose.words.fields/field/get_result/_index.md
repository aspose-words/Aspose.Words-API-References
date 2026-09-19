---
title: "Aspose::Words::Fields::Field::get_Result metodo"
linktitle: "get_Result"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::Field::get_Result metodo. Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.fields/field/get_result/
---
## Field::get_Result method


Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo.

```cpp
System::String Aspose::Words::Fields::Field::get_Result()
```


## Esempi



Mostra come inserire un campo in un documento utilizzando un codice di campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Questa variante del metodo InsertField aggiorna automaticamente i campi inseriti.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## Vedi anche

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
