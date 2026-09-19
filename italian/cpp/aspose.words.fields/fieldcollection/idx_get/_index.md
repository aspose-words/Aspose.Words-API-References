---
title: "Metodo Aspose::Words::Fields::FieldCollection::idx_get"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldCollection::idx_get. Restituisce un campo all'indice specificato in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.fields/fieldcollection/idx_get/
---
## FieldCollection::idx_get method


Restituisce un campo all'indice specificato.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Fields::FieldCollection::idx_get(int32_t index)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | Un indice nella collezione. |
## Note


L'indice parte da zero.

Gli indici negativi sono consentiti e indicano l'accesso dalla fine della collezione. Per esempio, -1 indica l'ultimo elemento, -2 il penultimo e così via.

Se l'indice è maggiore o uguale al numero di elementi nella lista, questo restituisce un riferimento nullo.

Se l'indice è negativo e il suo valore assoluto è maggiore del numero di elementi nella lista, questo restituisce un riferimento nullo.

## Esempi



Mostra come rimuovere i campi da una raccolta di campi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder->InsertField(u" TIME ");
builder->InsertField(u" REVNUM ");
builder->InsertField(u" AUTHOR  \"John Doe\" ");
builder->InsertField(u" SUBJECT \"My Subject\" ");
builder->InsertField(u" QUOTE \"Hello world!\" ");
doc->UpdateFields();

System::SharedPtr<Aspose::Words::Fields::FieldCollection> fields = doc->get_Range()->get_Fields();

ASSERT_EQ(6, fields->get_Count());

// Di seguito sono riportati quattro modi per rimuovere i campi da una raccolta di campi.
// 1 -  Ottieni un campo per rimuoversi da solo:
fields->idx_get(0)->Remove();
ASSERT_EQ(5, fields->get_Count());

// 2 -  Ottieni la raccolta per rimuovere un campo che passiamo al suo metodo di rimozione:
System::SharedPtr<Aspose::Words::Fields::Field> lastField = fields->idx_get(3);
fields->Remove(lastField);
ASSERT_EQ(4, fields->get_Count());

// 3 -  Rimuovi un campo da una raccolta a un indice:
fields->RemoveAt(2);
ASSERT_EQ(3, fields->get_Count());

// 4 -  Rimuovi tutti i campi dalla raccolta in una volta:
fields->Clear();
ASSERT_EQ(0, fields->get_Count());
```

## Vedi anche

* Class [Field](../../field/)
* Class [FieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
