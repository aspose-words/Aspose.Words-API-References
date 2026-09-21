---
title: "Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat metod"
linktitle: "get_LegacyNumberFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat method. Hämtar eller anger värdet som visar om det äldre (tidigare än AW 13.10) talformatet för fält är aktiverat eller inte i C++."
type: docs
weight: 16000
url: /sv/cpp/aspose.words.fields/fieldoptions/get_legacynumberformat/
---
## FieldOptions::get_LegacyNumberFormat method


Hämtar eller anger värdet som indikerar om äldre (tidigare än AW 13.10) talformat för fält är aktiverat eller inte.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat() const
```

## Anmärkningar


När den här egenskapen är satt till **true**, fungerar mallsymbolen \"#\" som i .net: Ersätter pundtecknet med motsvarande siffra om en sådan finns; annars visas inga symboler i resultatsträngen.

När den här egenskapen är satt till **false**, fungerar mallsymbolen \"#\" som i MS Word: Detta formatobjekt anger de nödvändiga numeriska positionerna som ska visas i resultatet. Om resultatet inte innehåller en siffra på den positionen visar MS Word ett mellanslag. Till exempel, { =  9 + 6 \\# $### } visar $ 15.

Standardvärdet är **false**.

## Exempel



Visar hur man aktiverar äldre talformatering för fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3 \\# $##");

ASSERT_EQ(u"$ 5", field->get_Result());

doc->get_FieldOptions()->set_LegacyNumberFormat(true);
field->Update();

ASSERT_EQ(u"$5", field->get_Result());
```

## Se även

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
