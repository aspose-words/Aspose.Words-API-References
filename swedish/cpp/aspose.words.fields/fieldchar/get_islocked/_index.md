---
title: "Aspose::Words::Fields::FieldChar::get_IsLocked metod"
linktitle: "get_IsLocked"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldChar::get_IsLocked metod. Hämtar eller anger om det överordnade fältet är låst (bör inte beräkna om sitt resultat) i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.fields/fieldchar/get_islocked/
---
## FieldChar::get_IsLocked method


Hämtar eller anger om föräldrafältet är låst (bör inte beräkna om sitt resultat).

```cpp
bool Aspose::Words::Fields::FieldChar::get_IsLocked() const
```


## Exempel



Visar hur man arbetar med en [FieldStart](../../fieldstart/) nod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->get_Format()->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

System::SharedPtr<Aspose::Words::Fields::FieldChar> fieldStart = field->get_Start();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, fieldStart->get_FieldType());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsDirty());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsLocked());

// Hämta fasadobjektet som representerar fältet i dokumentet.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(false, field->get_IsLocked());
ASSERT_EQ(u" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Uppdatera fältet så att det visar det aktuella datumet.
field->Update();
```

## Se även

* Class [FieldChar](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
