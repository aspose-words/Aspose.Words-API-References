---
title: "Aspose::Words::Fields::FieldAddressBlock::get_ExcludedCountryOrRegionName Methode"
linktitle: "get_ExcludedCountryOrRegionName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldAddressBlock::get_ExcludedCountryOrRegionName Methode. Gibt den ausgeschlossenen Länder-/Regionsnamen in C++ zurück oder legt ihn fest."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fields/fieldaddressblock/get_excludedcountryorregionname/
---
## FieldAddressBlock::get_ExcludedCountryOrRegionName method


Ruft den ausgeschlossenen Länder-/Regionsnamen ab oder legt ihn fest.

```cpp
System::String Aspose::Words::Fields::FieldAddressBlock::get_ExcludedCountryOrRegionName()
```


## Beispiele



Zeigt, wie man ein ADDRESSBLOCK-Feld einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAddressBlock>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAddressBlock, true));

ASSERT_EQ(u" ADDRESSBLOCK ", field->GetFieldCode());

// Wenn man dies auf "2" setzt, werden alle Länder und Regionen einbezogen,
// es sei denn, es ist das in der Eigenschaft ExcludedCountryOrRegionName angegebene.
field->set_IncludeCountryOrRegionName(u"2");
field->set_FormatAddressOnCountryOrRegion(true);
field->set_ExcludedCountryOrRegionName(u"United States");
field->set_NameAndAddressFormat(u"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>");

// Standardmäßig enthält diese Eigenschaft die Sprach-ID des ersten Zeichens des Dokuments.
// Wir können für das Feld eine andere Kultur festlegen, um das Ergebnis wie folgt zu formatieren.
field->set_LanguageId(System::Convert::ToString(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID()));

ASSERT_EQ(u" ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033", field->GetFieldCode());
```

## Siehe auch

* Class [FieldAddressBlock](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
