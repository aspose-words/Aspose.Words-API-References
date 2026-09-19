---
title: "Aspose::Words::Fields::Field::get_Type method"
linktitle: "get_Type"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::Field::get_Type method. Ottiene il tipo di campo di Microsoft Word in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.fields/field/get_type/
---
## Field::get_Type method


Restituisce il tipo di campo di Microsoft Word.

```cpp
virtual Aspose::Words::Fields::FieldType Aspose::Words::Fields::Field::get_Type() const
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

* Enum [FieldType](../../fieldtype/)
* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
