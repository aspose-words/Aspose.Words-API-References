---
title: "Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat metod"
linktitle: "get_UseInvariantCultureNumberFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat metod. Hämtar eller anger värdet som indikerar om talformatet tolkas med invariant kultur eller inte i C++."
type: docs
weight: 21000
url: /sv/cpp/aspose.words.fields/fieldoptions/get_useinvariantculturenumberformat/
---
## FieldOptions::get_UseInvariantCultureNumberFormat method


Hämtar eller anger värdet som indikerar om talformat tolkas med invariant kultur eller inte.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat() const
```

## Anmärkningar


När den här egenskapen är inställd på **true**, tas talformatet från en invariant kultur.

När den här egenskapen är inställd på **false**, tas talformatet från den aktuella trådens kultur.

Standardvärdet är **false**.

## Exempel



Visar hur man formaterar tal enligt den invariant kulturen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::Threading::Thread::get_CurrentThread()->set_CurrentCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" = 1234567,89 \\# $#,###,###.##");
field->Update();

// Ibland kan fält inte formatera sina tal korrekt under vissa kulturer.
ASSERT_FALSE(doc->get_FieldOptions()->get_UseInvariantCultureNumberFormat());
ASSERT_EQ(u"$1.234.567,89 ,     ", field->get_Result());

// För att åtgärda detta kan vi ändra kulturen för hela tråden.
// Ett annat sätt att åtgärda detta är att sätta den här flaggan,
// vilket får alla fält att använda den invariant kulturen när de formaterar tal.
// Detta sätt gör att vi kan undvika att ändra kulturen för hela tråden.
doc->get_FieldOptions()->set_UseInvariantCultureNumberFormat(true);
field->Update();
ASSERT_EQ(u"$1.234.567,89", field->get_Result());
```

## Se även

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
