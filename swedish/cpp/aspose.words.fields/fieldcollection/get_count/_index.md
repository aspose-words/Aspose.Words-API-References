---
title: "Aspose::Words::Fields::FieldCollection::get_Count metod"
linktitle: "get_Count"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldCollection::get_Count metod. Returnerar antalet fält i samlingen i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.fields/fieldcollection/get_count/
---
## FieldCollection::get_Count method


Returnerar antalet fält i samlingen.

```cpp
int32_t Aspose::Words::Fields::FieldCollection::get_Count()
```


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

* Class [FieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
