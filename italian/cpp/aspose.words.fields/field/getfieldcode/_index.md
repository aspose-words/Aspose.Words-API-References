---
title: "Aspose::Words::Fields::Field::GetFieldCode metodo"
linktitle: "GetFieldCode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::Field::GetFieldCode metodo. Restituisce il testo compreso tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sia il codice del campo sia il risultato dei campi figli sono inclusi in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.fields/field/getfieldcode/
---
## Field::GetFieldCode() method


Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio.

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode()
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


Mostra come ottenere il codice di un campo.
```cpp
// Apri un documento che contiene un MERGEFIELD all'interno di un campo IF.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// Ci sono due modi per ottenere il codice di un campo:
// 1 -  Omettere i suoi campi interni:
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  Includere i suoi campi interni:
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// Per impostazione predefinita, il metodo GetFieldCode visualizza i campi interni.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## Vedi anche

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## Field::GetFieldCode(bool) method


Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore).

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode(bool includeChildFieldCodes)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| includeChildFieldCodes | bool | **true** se i codici dei campi figli devono essere inclusi. |

## Esempi



Mostra come ottenere il codice di un campo.
```cpp
// Apri un documento che contiene un MERGEFIELD all'interno di un campo IF.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// Ci sono due modi per ottenere il codice di un campo:
// 1 -  Omettere i suoi campi interni:
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  Includere i suoi campi interni:
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// Per impostazione predefinita, il metodo GetFieldCode visualizza i campi interni.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## Vedi anche

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
