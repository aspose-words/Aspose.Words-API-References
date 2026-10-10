---
title: "Aspose::Words::Range::NormalizeFieldTypes method"
linktitle: "NormalizeFieldTypes"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Range::NormalizeFieldTypes. Modifica i valori del tipo di campo FieldType di FieldStart, FieldSeparator, FieldEnd in questo intervallo in modo che corrispondano ai tipi di campo contenuti nei codici di campo in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words/range/normalizefieldtypes/
---
## Range::NormalizeFieldTypes method


Modifica i valori del tipo di campo [FieldType](../../../aspose.words.fields/fieldchar/get_fieldtype/) di [FieldStart](../../../aspose.words.fields/fieldstart/), [FieldSeparator](../../../aspose.words.fields/fieldseparator/), [FieldEnd](../../../aspose.words.fields/fieldend/) in questo intervallo in modo che corrispondano ai tipi di campo contenuti nei codici di campo.

```cpp
void Aspose::Words::Range::NormalizeFieldTypes()
```

## Note


Utilizza questo metodo dopo le modifiche al documento che influenzano i tipi di campo.

Per modificare i valori del tipo di campo nell'intero documento, usa [NormalizeFieldTypes](../../document/normalizefieldtypes/).

## Esempi



Mostra come mantenere aggiornato il tipo di un campo rispetto al suo codice di campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE", nullptr);

// Aspose.Words rileva automaticamente i tipi di campo in base ai codici di campo.
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());

// Modifica manualmente il testo grezzo del campo, che determina il codice del campo.
auto fieldText = System::ExplicitCast<Aspose::Words::Run>(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(0));
fieldText->set_Text(u"PAGE");

// La modifica del codice del campo ha trasformato questo campo in uno di tipo diverso,
// ma le proprietà del tipo del campo mostrano ancora il tipo precedente.
ASSERT_EQ(u"PAGE", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_End()->get_FieldType());

// Aggiorna tali proprietà con questo metodo per visualizzare il valore corrente.
doc->NormalizeFieldTypes();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_End()->get_FieldType());
```

## Vedi anche

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
