---
title: "Aspose::Words::Fields::FieldAddressBlock::get_LanguageId metod"
linktitle: "get_LanguageId"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldAddressBlock::get_LanguageId metod. Hämtar eller anger språk‑ID‑t som används för att formatera adressen i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.fields/fieldaddressblock/get_languageid/
---
## FieldAddressBlock::get_LanguageId method


Hämtar eller anger språk‑ID som används för att formatera adressen.

```cpp
System::String Aspose::Words::Fields::FieldAddressBlock::get_LanguageId()
```


## Exempel



Visar hur man infogar ett ADDRESSBLOCK‑fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAddressBlock>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAddressBlock, true));

ASSERT_EQ(u" ADDRESSBLOCK ", field->GetFieldCode());

// Om du ställer in detta på "2" kommer alla länder och regioner att inkluderas,
// såvida det inte är den som anges i egenskapen ExcludedCountryOrRegionName.
field->set_IncludeCountryOrRegionName(u"2");
field->set_FormatAddressOnCountryOrRegion(true);
field->set_ExcludedCountryOrRegionName(u"United States");
field->set_NameAndAddressFormat(u"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>");

// Som standard kommer den här egenskapen att innehålla språk-ID:t för det första tecknet i dokumentet.
// Vi kan ange en annan kultur för fältet för att formatera resultatet så här.
field->set_LanguageId(System::Convert::ToString(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID()));

ASSERT_EQ(u" ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033", field->GetFieldCode());
```

## Se även

* Class [FieldAddressBlock](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
