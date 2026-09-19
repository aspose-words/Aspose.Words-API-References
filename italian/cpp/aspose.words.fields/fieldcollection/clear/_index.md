---
title: "Metodo Aspose::Words::Fields::FieldCollection::Clear"
linktitle: "Cancella"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldCollection::Clear. Rimuove tutti i campi di questa collezione dal documento e dalla stessa collezione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldcollection/clear/
---
## FieldCollection::Clear method


Rimuove tutti i campi di questa raccolta dal documento e dalla stessa raccolta.

```cpp
void Aspose::Words::Fields::FieldCollection::Clear()
```


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

* Class [FieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
