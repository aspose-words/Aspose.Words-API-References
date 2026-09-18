---
title: "Aspose::Words::Fields::FieldCollection::get_Count Methode"
linktitle: "get_Count"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldCollection::get_Count Methode. Gibt die Anzahl der Felder in der Sammlung in C++ zurück."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fields/fieldcollection/get_count/
---
## FieldCollection::get_Count method


Gibt die Anzahl der Felder in der Sammlung zurück.

```cpp
int32_t Aspose::Words::Fields::FieldCollection::get_Count()
```


## Beispiele



Zeigt, wie man Felder aus einer Feldsammlung entfernt.
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

// Unten sind vier Methoden zum Entfernen von Feldern aus einer Feldsammlung aufgeführt.
// 1 -  Ein Feld erhalten, das sich selbst entfernt:
fields->idx_get(0)->Remove();
ASSERT_EQ(5, fields->get_Count());

// 2 -  Die Sammlung erhalten, um ein Feld zu entfernen, das wir ihrer Entfernungs‑Methode übergeben:
System::SharedPtr<Aspose::Words::Fields::Field> lastField = fields->idx_get(3);
fields->Remove(lastField);
ASSERT_EQ(4, fields->get_Count());

// 3 -  Ein Feld aus einer Sammlung an einem Index entfernen:
fields->RemoveAt(2);
ASSERT_EQ(3, fields->get_Count());

// 4 -  Alle Felder aus der Sammlung auf einmal entfernen:
fields->Clear();
ASSERT_EQ(0, fields->get_Count());
```

## Siehe auch

* Class [FieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
