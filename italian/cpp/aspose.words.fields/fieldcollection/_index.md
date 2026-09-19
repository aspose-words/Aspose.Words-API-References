---
title: "Aspose::Words::Fields::FieldCollection class"
linktitle: "FieldCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldCollection class. Una raccolta di oggetti Field che rappresenta i campi nell'intervallo specificato. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 23000
url: /it/cpp/aspose.words.fields/fieldcollection/
---
## FieldCollection class


Una raccolta di oggetti [Field](../field/) che rappresenta i campi nell'intervallo specificato. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::Field>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Clear](./clear/)() | Rimuove tutti i campi di questa raccolta dal documento e dalla stessa raccolta. |
| [get_Count](./get_count/)() | Restituisce il numero dei campi nella raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Restituisce un campo all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&) | Rimuove il campo specificato da questa raccolta e dal documento. |
| [RemoveAt](./removeat/)(int32_t) | Rimuove un campo all'indice specificato da questa raccolta e dal documento. |
| static [Type](./type/)() |  |
## Note


Un'istanza di questa raccolta itera i campi che iniziano all'interno dell'intervallo specificato.

La raccolta [FieldCollection](./) non possiede i campi che contiene, ma è semplicemente una selezione di campi.

La raccolta [FieldCollection](./) è "live", cioè le modifiche ai figli dell'oggetto nodo da cui è stata creata sono immediatamente riflesse nei campi restituiti dalle proprietà e metodi di [FieldCollection](./).

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

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
