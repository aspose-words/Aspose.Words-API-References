---
title: "Aspose::Words::Fields::FieldCollection class"
linktitle: "FieldCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldCollection class. En samling av Field-objekt som representerar fälten i det angivna intervallet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 23000
url: /sv/cpp/aspose.words.fields/fieldcollection/
---
## FieldCollection class


En samling av [Field](../field/) objekt som representerar fälten i det angivna intervallet. För att lära dig mer, besök dokumentationsartikeln [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::Field>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Clear](./clear/)() | Tar bort alla fält i denna samling från dokumentet och från själva samlingen. |
| [get_Count](./get_count/)() | Returnerar antalet fält i samlingen. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returnerar ett fält på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&) | Tar bort det angivna fältet från denna samling och från dokumentet. |
| [RemoveAt](./removeat/)(int32_t) | Tar bort ett fält på det angivna indexet från denna samling och från dokumentet. |
| static [Type](./type/)() |  |
## Anmärkningar


En instans av denna samling itererar fält som börjar inom det angivna intervallet.

Samlingen [FieldCollection](./) äger inte fälten den innehåller, utan är bara ett urval av fält.

Samlingen [FieldCollection](./) är "live", d.v.s. förändringar i barnen till nodobjektet som den skapades från återspeglas omedelbart i fälten som returneras av [FieldCollection](./)-egenskaperna och -metoderna.

## Exempel



Visar hur man tar bort fält från en fältssamling.
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

// Nedan följer fyra sätt att ta bort fält från en fältssamling.
// 1 -  Hämta ett fält för att ta bort sig själv:
fields->idx_get(0)->Remove();
ASSERT_EQ(5, fields->get_Count());

// 2 -  Hämta samlingen för att ta bort ett fält som vi skickar till dess borttagningsmetod:
System::SharedPtr<Aspose::Words::Fields::Field> lastField = fields->idx_get(3);
fields->Remove(lastField);
ASSERT_EQ(4, fields->get_Count());

// 3 -  Ta bort ett fält från en samling på ett index:
fields->RemoveAt(2);
ASSERT_EQ(3, fields->get_Count());

// 4 -  Ta bort alla fält från samlingen på en gång:
fields->Clear();
ASSERT_EQ(0, fields->get_Count());
```

## Se även

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
